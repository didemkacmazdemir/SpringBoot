# SpringBoot
Spring Boot reduces the need to write a lot of configuration and boilerplate code.

What is application contex?

Most important thing is all Spring beans are managed, and "live" inside a container, called "application context".What is "living" in the application context? This means that the context instantiates the objects.(creates object with new keyword)
Application context is bootstrapped(başlatma) and all beans - autowired. In web applications this can be a startup listener.

@Autowired

Bir sınıfta başka bir sınıfa ihtiyaç duyulması durumu kaçınılmazdır. Spring’ in temel çıkış noktalarından birisi olan dependency injection ise bu durumda vazgeçilmez vazgeçilmemesi gereken bir tasarım olarak ortaya çıkıyor. Yani A nesnesi ihtiyaç duyduğu B nesnesini direkt olarak constructor veya set metotları aracılığı ile kabul edecektir.

@Component 
 
 This is a general-purpose stereotype annotation indicating that the class is a spring component.
 --it’s not wrong to say that @Controller, @Service and @Repository are special types of @Component annotation.--
 
@Repository
 
This is Persistence layer(Data Access Layer) of application which used to get data from the database. i.e. all the Database related operations are done by the repository.
 
@Service   

All business logic is here i.e. Data related calculations and all.This annotation of business layer in which our user not directly call persistence method so it will call this method using this annotation                     

@Controller 

where your request mapping from presentation page done i.e. Presentation layer won't go to any other file it goes directly to @Controller class and checks for requested path in @RequestMapping annotation which written before method calls if necessary

@Entity 

ile işaretlediğiniz sınıflar için, veritabanında tabloları ve sütunlarını otomatik oluşturur.Yada @Entity sınıf ile veritabanındaki tabloyu eşleştirecektir.

@Data 
notu bizim yerimize getter ve setter metodlarını oluşturacak

Ornek Entity Class
@Data
@Entity
public class Customer {
    @Id
    @GeneratedValue
    private Long id;
    private int age;
    private String name;
    Customer() {}
    public Customer(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

@JsonIgnore
The Jackson annotation @JsonIgnore is used to tell Jackson to ignore a certain property (field) of a Java objec




