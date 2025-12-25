# Techsprint-hackathon
import React from 'react';
import { Link } from 'react-router-dom';
import { Button } from '@/components/ui/button';
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from '@/components/ui/card';
import { Badge } from '@/components/ui/badge';
import { 
  Stethoscope, 
  Users, 
  Pill, 
  Bell, 
  Shield, 
  Clock,
  ArrowRight,
  CheckCircle2,
  Activity,
  Heart
} from 'lucide-react';

const features = [
  {
    icon: <Bell className="w-6 h-6" />,
    title: 'Real-time Alerts',
    description: 'Instant communication between patients and doctors for timely care',
  },
  {
    icon: <Shield className="w-6 h-6" />,
    title: 'Medicine Safety',
    description: 'Automated verification prevents wrong or expired medicine delivery',
  },
  {
    icon: <Users className="w-6 h-6" />,
    title: 'Smart Routing',
    description: 'Auto-assign patients to the right department and doctor',
  },
  {
    icon: <Clock className="w-6 h-6" />,
    title: 'Queue Management',
    description: 'Efficient patient flow with real-time queue status updates',
  },
];

const roles = [
  {
    icon: <Users className="w-8 h-8" />,
    title: 'Patient Portal',
    description: 'View appointments, send alerts, track prescriptions',
    color: 'bg-accent',
  },
  {
    icon: <Stethoscope className="w-8 h-8" />,
    title: 'Doctor Dashboard',
    description: 'Manage patients, respond to alerts, prescribe medicines',
    color: 'bg-primary',
  },
  {
    icon: <Pill className="w-8 h-8" />,
    title: 'Staff Console',
    description: 'Verify medicines, manage inventory, dispense safely',
    color: 'bg-success',
  },
];

const Index: React.FC = () => {
  return (
    <div className="min-h-screen">
      {/* Hero Section */}
<section className="relative gradient-hero overflow-hidden">
<div className="absolute inset-0 bg-grid-pattern opacity-5" />
<div className="container mx-auto px-4 py-16 md:py-24">
<div className="max-w-4xl mx-auto text-center animate-slide-up">
<Badge variant="default" className="mb-4">
<Activity className="w-3 h-3 mr-1" />
Healthcare Innovation
</Badge>
        <h1 className="text-4xl md:text-6xl font-bold text-foreground mb-6 leading-tight">
Smart Hospital
       <span className="block text-primary">
Information System
</span>
            </h1>
            <p className="text-lg md:text-xl text-muted-foreground mb-8 max-w-2xl mx-auto">
              Bridging the gap between doctors and patients with real-time communication, 
              medicine safety verification, and intelligent patient routing.
            </p>
            <div className="flex flex-col sm:flex-row gap-4 justify-center">
              <Link to="/login">
                <Button size="xl" variant="hero">
    Get Started
   <ArrowRight className="w-5 h-5 ml-2" />
            </Button>
            </Link>
            <Button size="xl" variant="outline">
            Learn More
            </Button>
            </div>
            </div>
{/* Stats */}
<div className="grid grid-cols-2 md:grid-cols-4 gap-4 mt-16 max-w-3xl mx-auto">
            {[
              { value: '24/7', label: 'Availability' },
              { value: '< 1s', label: 'Alert Time' },
              { value: '100%', label: 'Safety Check' },
              { value: '3+', label: 'User Roles' },
            ].map((stat, idx) => (
<div key={idx} className="text-center p-4">
<p className="text-3xl font-bold text-primary">{stat.value}</p>
<p className="text-sm text-muted-foreground">{stat.label}</p>
</div>
))}
    </div>
    </div>
    </section>

      {/* Features Section */}
      <section className="py-16 md:py-24 bg-background">
            <div className="container mx-auto px-4">
            <div className="text-center mb-12">
            <Badge variant="secondary" className="mb-4">Features</Badge>
            <h2 className="text-3xl md:text-4xl font-bold mb-4">
Solving Real Hospital Problems
             </h2>
             <p className="text-muted-foreground max-w-2xl mx-auto">
             Our system addresses critical challenges in doctor-patient communication,
             medicine safety, and patient guidance.
             </p>
             </div>

          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            {features.map((feature, idx) => (
              <Card key={idx} variant="interactive" className="text-center">
              <CardHeader>
              <div className="w-14 h-14 mx-auto rounded-2xl bg-primary/10 flex items-center justify-center text-primary mb-2">
 {feature.icon}
                </div>
                <CardTitle className="text-lg">{feature.title}</CardTitle>
                </CardHeader>
                <CardContent>
<CardDescription>{feature.description}</CardDescription>
</CardContent>
</Card>
))}
</div>
</div>
</section>

      {/* Role-based Access */}
      <section className="py-16 md:py-24 bg-secondary/30">
        <div className="container mx-auto px-4">
     <div className="text-center mb-12">
     <Badge variant="secondary" className="mb-4">User Roles</Badge>
      <h2 className="text-3xl md:text-4xl font-bold mb-4">
      Three Dashboards, One System
            </h2>
            <p className="text-muted-foreground max-w-2xl mx-auto">
            Each user role has a tailored dashboard designed for their specific needs.
            </p>
            </div>

          <div className="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
            {roles.map((role, idx) => (
              <Card key={idx} variant="elevated">
                <CardHeader>
      <div className={`w-16 h-16 rounded-2xl ${role.color} flex items-center justify-center text-primary-foreground mb-4`}>
               {role.icon}
                  </div>
                  <CardTitle>{role.title}</CardTitle>
                  <CardDescription>{role.description}</CardDescription>
                </CardHeader>
                <CardContent>
                  <ul className="space-y-2">
                    {['Role-based access', 'Mobile responsive', 'Real-time updates'].map((item, i) => (
                    <li key={i} className="flex items-center gap-2 text-sm text-muted-foreground">
   <CheckCircle2 className="w-4 h-4 text-success" />
    {item}
    </li>
    ))}
  </ul>
  /CardContent>
  </Card>
  ))}
  </div>
        </div>
      </section>

      {/* CTA Section */}
      <section className="py-16 md:py-24 bg-background">
        <div className="container mx-auto px-4">
  <Card variant="elevated" className="max-w-4xl mx-auto overflow-hidden">
  <div className="gradient-primary p-8 md:p-12 text-center">
  <Heart className="w-12 h-12 mx-auto mb-4 text-primary-foreground" />
  <h2 className="text-2xl md:text-3xl font-bold text-primary-foreground mb-4">
    Ready to Transform Healthcare?
              </h2>
              <p className="text-primary-foreground/80 mb-6 max-w-xl mx-auto">
                Experience the future of hospital management with our smart information system.
              </p>
              <Link to="/login">
                <Button size="xl" variant="secondary">
Start Demo Now
<ArrowRight className="w-5 h-5 ml-2" />
</Button>
</Link>
</div>
</Card>
</div>
</section>

      {/* Footer */}
      <footer className="border-t py-8">
  <div className="container mx-auto px-4">
  <div className="flex flex-col md:flex-row items-center justify-between gap-4">
  <div className="flex items-center gap-2">
<div className="w-8 h-8 rounded-lg gradient-primary flex items-center justify-center">
<Stethoscope className="w-4 h-4 text-primary-foreground" />
</div>
              <span className="font-semibold">Smart Hospital System</span>
            </div>
            <p className="text-sm text-muted-foreground">
              © 2024 Smart Hospital Information System. Built for Healthcare Innovation.
  </p>
  </div>
  </div>
  </footer>
  </div>
  );
};

export default Index;
