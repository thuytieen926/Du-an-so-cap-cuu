import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs"; import { Input } from "@/components/ui/input"; import { Label } from "@/components/ui/label"; import { Textarea } from "@/components/ui/textarea";

export default function HomePage() { return ( <main className="min-h-screen bg-white text-gray-800"> <section className="bg-red-500 text-white py-10 px-6 text-center"> <h1 className="text-4xl font-bold mb-2">Một Hành Động - Một Mạng Sống</h1> <p className="text-lg">Dự án nâng cao nhận thức và kỹ năng sơ cấp cứu cho cộng đồng</p> </section>

<Tabs defaultValue="intro" className="px-4 py-8">
    <TabsList className="grid grid-cols-5 bg-blue-100">
      <TabsTrigger value="intro">Giới thiệu</TabsTrigger>
      <TabsTrigger value="products">Sản phẩm</TabsTrigger>
      <TabsTrigger value="register">Đăng ký lớp học</TabsTrigger>
      <TabsTrigger value="order">Đặt hàng</TabsTrigger>
      <TabsTrigger value="feedback">Phản hồi</TabsTrigger>
    </TabsList>

    <TabsContent value="intro">
      <section className="max-w-3xl mx-auto mt-6">
        <h2 className="text-2xl font-semibold mb-4 text-red-600">Về dự án</h2>
        <p>
          "Một Hành Động - Một Mạng Sống" là dự án khởi nghiệp với sứ mệnh phổ cập kiến thức sơ cấp cứu và cung cấp những công cụ cần thiết để mỗi người dân đều có thể hỗ trợ trong tình huống khẩn cấp. Chúng tôi tổ chức các lớp học sơ cứu và cung cấp bộ kit sơ cấp cứu tiện lợi cho hộ gia đình, học sinh và người đi đường.
        </p>
      </section>
    </TabsContent>

    <TabsContent value="products">
      <section className="grid md:grid-cols-2 gap-4 mt-6 px-2">
        <Card className="bg-white border shadow-md">
          <CardContent className="p-4">
            <h3 className="text-xl font-semibold text-blue-700">Bộ Kit Sơ Cấp Cứu Cơ Bản</h3>
            <ul className="list-disc list-inside mt-2 text-gray-700">
              <li>Băng gạc, bông, băng keo y tế</li>
              <li>Cồn, iốt sát trùng</li>
              <li>Kéo y tế, găng tay, nẹp cố định</li>
              <li>Sách hướng dẫn sơ cứu</li>
            </ul>
            <p className="mt-4 text-red-600 font-bold">Giá: 150.000đ</p>
            <Button className="mt-2 bg-red-500 hover:bg-red-600">Mua ngay</Button>
          </CardContent>
        </Card>
      </section>
    </TabsContent>

    <TabsContent value="register">
      <section className="max-w-xl mx-auto mt-6">
        <h2 className="text-2xl font-semibold text-red-600 mb-4">Đăng ký lớp học sơ cứu</h2>
        <form className="space-y-4">
          <div>
          <Label htmlFor="name">Họ và tên</Label>
            <Input id="name" placeholder="Nhập họ tên của bạn" />
          </div>
          <div>
            <Label htmlFor="email">Email</Label>
            <Input id="email" type="email" placeholder="example@email.com" />
          </div>
          <div>
            <Label htmlFor="phone">Số điện thoại</Label>
            <Input id="phone" type="tel" placeholder="0123 456 789" />
          </div>
          <div>
            <Label htmlFor="message">Ghi chú (nếu có)</Label>
            <Textarea id="message" placeholder="Ví dụ: Muốn học vào cuối tuần" />
          </div>
          <Button className="bg-blue-600 hover:bg-blue-700">Gửi đăng ký</Button>
        </form>
      </section>
    </TabsContent>

    <TabsContent value="order">
      <section className="max-w-xl mx-auto mt-6">
        <h2 className="text-2xl font-semibold text-red-600 mb-4">Đặt mua bộ kit sơ cấp cứu</h2>
        <form className="space-y-4">
          <div>
            <Label htmlFor="fullname">Họ và tên</Label>
            <Input id="fullname" placeholder="Nhập họ tên của bạn" />
          </div>
          <div>
            <Label htmlFor="address">Địa chỉ nhận hàng</Label>
            <Input id="address" placeholder="Số nhà, đường, quận, thành phố..." />
          </div>
          <div>
            <Label htmlFor="phone_order">Số điện thoại</Label>
            <Input id="phone_order" type="tel" placeholder="0123 456 789" />
          </div>
          <div>
            <Label htmlFor="quantity">Số lượng</Label>
            <Input id="quantity" type="number" min="1" defaultValue="1" />
          </div>
          <Button className="bg-green-600 hover:bg-green-700">Gửi đơn hàng</Button>
        </form>
      </section>
    </TabsContent>

    <TabsContent value="feedback">
      <section className="max-w-3xl mx-auto mt-6 px-2">
        <h2 className="text-2xl font-semibold text-red-600 mb-4">Phản hồi từ người dùng</h2>
        <Card className="mb-4">
          <CardContent className="p-4">
            <p className="italic">“Bộ kit rất tiện dụng, tôi cảm thấy yên tâm hơn khi có trong nhà.”</p>
            <p className="mt-2 font-semibold text-blue-700">— Chị Mai, quận 7</p>
          </CardContent>
        </Card>
        <Card>
          <CardContent className="p-4">
            <p className="italic">“Lớp học sơ cứu dễ hiểu, giúp tôi biết cách xử lý khi gặp tai nạn bất ngờ.”</p>
            <p className="mt-2 font-semibold text-blue-700">— Anh Long, sinh viên</p>
          </CardContent>
        </Card>
      </section>
    </TabsContent>
  </Tabs>
</main>

); }
