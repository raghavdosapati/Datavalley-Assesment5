import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;

public class DepartmentDB {

    public static void main(String[] args) throws Exception {
        Connection connection = null;
        Statement statement = null;

        String username = "Username";
        String password = "Password";
        Department department = new Department(07, "computers");

        try {
            Class.forName("com.mysql.cj.jdbc.Driver");
            connection = DriverManager.getConnection(Username, Password);
            statement = connection.createStatement();
            String sql = "INSERT INTO department (id, name) VALUES (" + department.getId() + ", '" + department.getName() + "')";
            statement.executeUpdate(sql);
            System.out.println("Department " + department.getName() + " stored successfully!");

        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            if (statement != null) {
                statement.close();
            }
            if (connection != null) {
                connection.close();
            }
        }
    }
}

class Department {
    private int id;
    private String name;

    public Department(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public int getId() {
        return id;
    }

    public String getName() {
        return name;
    }
}
