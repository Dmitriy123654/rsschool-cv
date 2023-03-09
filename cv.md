# [rsschool-cv](https://app.rs.school/)

# Ermak Dmitriy

## C# Backend Developer

---

# Contact information

Phone: +375336896267

E-mail: dimaermak06@gmail.com

Telegram: [@ermaakkk](https://t.me/ermaakkk "клик")

LinkedIn: [Ermak Dmitriy](https://www.linkedin.com/in/ermakdmitriy/ "всегда рад новым знакомствам)")

Github: [@Dmitriy123654](https://github.com/Dmitriy123654 "можешь глянуть чем я там занимаюсь")

Discord: Dima#8566

---

# About Myself:

Currently, I am a second-year student of the Belarusian State University of Informatics and Radioelectronics, studying at the Faculty of Information Technology and Management in the specialty "Automated Information processing systems".

I am an inquisitive person who always strives to learn and accept new challenges. In my free time from studies and courses, I do sports.

I am already familiar with such things as: C#, Entity Framework, MSSQL, MySQL, Razor Pages, network programming, Git; Аt a basic level I know HTML, CSS, ASP.NET , C++ .

I am currently studying ASP.NET and I'm starting to conquer the JS course, and I'm also working on improving my English language skills.

---

# Skills and Proficiency:

- MySQL,MSSQL
- C#, Visual Studio
  - Entity Framework
  - ASP.NET
  - Network programming
  - Razor Pages
- C++, Visual Studio
- HTML, CSS
- Git, Github

---

# Code example:

### Part of an example of creating a database in C# using Entity Framework

```
namespace WarehouseInformationSystem.Data
{
    public class ApplicationDbContext : DbContext
    {
        public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
            : base(options)
        { }
        public DbSet<Address> Addresses { get; set; } = null!;
        public DbSet<CategoryOfProduct> CategoryOfProducts { get; set; } = null!;
        public DbSet<Product> Products { get; set; } = null!;
        public DbSet<Location> Locations { get; set; } = null!;
        public DbSet<User> Users { get; set; } = null!;
        public DbSet<Employee> Employees { get; set; } = null!;
        public DbSet<Department> Departments { get; set; } = null!;
        public DbSet<Post> Posts { get; set; } = null!;
        protected override void OnModelCreating(ModelBuilder modelBuilder)
        {
            modelBuilder.Entity<Employee>().Property(p => p.Salary)
                .HasPrecision(20, 2);
            modelBuilder.Entity<Product>().Property(p => p.SalePrice)
                .HasPrecision(20, 2);
            modelBuilder.Entity<Product>().Property(p => p.PurchasePrice)
                .HasPrecision(20, 2);
        }
    }
    public class SampleContextFactory : IDesignTimeDbContextFactory<ApplicationDbContext>
    {
        public ApplicationDbContext CreateDbContext(string[] args)
        {
            var optionsBuilder = new DbContextOptionsBuilder<ApplicationDbContext>();

            var builder = WebApplication.CreateBuilder();
            string connectionString = builder.Configuration.GetConnectionString("DefaultConnection");
            var app = builder.Build();

            optionsBuilder.UseMySql(connectionString, ServerVersion.AutoDetect(connectionString));
            return new ApplicationDbContext(optionsBuilder.Options);
        }
    }
}
```

---

# Education

- 2nd year student at the Belarusian State University of Informatics and Radioelectronics, Faculty of Information Technology and Management, specialisation Automated Information Processing Systems
- in the future..

---

# Languages:

- Russian - Native
- Belarusian - Native
- English - Elementary

---
