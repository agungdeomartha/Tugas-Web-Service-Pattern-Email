# Tugas-Web-Service-Pattern-Email
Mohammad Agung Deomartha 1154032 D4TI2B

Penjelasa FIle JasaSewaKamera.xsd
didalam file JasaSewaKamera.xsd terdapat 5 data dimana masing masing datanya terdapat 10 elemen dan dengan elemen root bernama "<sewakamera>".

<xs:element name="sewakamera">
        <xs:complexType>
            <xs:choice maxOccurs="unbounded">
                <xs:element ref="alamat"/>
                <xs:element ref="denda"/>
                <xs:element ref="durasi"/>
                <xs:element ref="email"/>
                <xs:element ref="harga"/>
                <xs:element ref="id"/>
                <xs:element ref="jeniskamera"/>
                <xs:element ref="peminjam"/>
                <xs:element ref="tglkembali"/>
                <xs:element ref="tglsewa"/>
            </xs:choice>
          
        </xs:complexType>
    </xs:element>
    
    
   Yang perlu diperhatikan didalam file JasaSewaKamera.xsd ini memiliki element <email> yang telah diberikan pattern untuk memvalidasi format email.
   Berikut Syntax yang di input untuk membuat pattern email pada elemen <email> :
   <xs:element name="email">
    	<xs:simpleType>
    		<xs:restriction base="xs:string">
    			<xs:pattern
    				value="[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}">
    			</xs:pattern>
    		</xs:restriction>
    	</xs:simpleType>
    </xs:element>
    
    perhatikan syntax diatas memiliki pattern dengan value="[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}">
    nilai value tersebutlah yang akan memformat format email yang sah. Misalnya jika tidak diinputkan karakter "@" dan ".(namadomain) atau jika tidak diinputkan karakter yang sesuai Maka pada saat proses validasi akan muncul peringatan Error, Atau tidak Valid.
