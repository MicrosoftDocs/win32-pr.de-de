---
title: Programmieren von ADSI mit Java/COM
description: Mithilfe des virtuellen Microsoft-Computers für Java (Microsoft-VM) und des Microsoft Java Compilers haben Sie Zugriff auf alle ADSI-Features, die über ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmieren von ADSI mit Java/COM AD
- ADSI ADSI mit, Java/COM-Programmierung für
- ADSI ADSI , Beispielcode Java
- ADSI ADSI , Beispielcode Java, Bindung an ein ADSI-Objekt und Aufrufen von Methoden für dieses Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec873822d27a7b5fcf95aad7c31a8978552eb88
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880292"
---
# <a name="programming-adsi-with-javacom"></a>Programmieren von ADSI mit Java/COM

Mithilfe des virtuellen Microsoft-Computers für Java (Microsoft-VM) und des Microsoft Java Compilers haben Sie Zugriff auf alle ADSI-Features, die über ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden. Das folgende Java-Codebeispiel zeigt die Elemente, die zum Binden an ein ADSI-Objekt und Aufrufen von Methoden für dieses Objekt erforderlich sind. Die erforderlichen ADSI-API-Funktionen und -Objektmethoden werden über Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



Das Argument in der ersten **import-Anweisung** bezieht sich auf Java Wrapper-Klassen, die in Activeds.dll. Verwenden Sie Visual J++, um die Wrapperklassen zu erstellen und sie in Ihr Projekt ein include zu lassen, wie unten beschrieben.

**So erstellen Sie Wrapperklassen und schließen sie in Ihr Projekt ein**

1.  Wählen Sie in einem Visual J++-Projekt **com Wrapper hinzufügen...** im **menü** Project aus.
2.  Wählen Sie im Dialogfeld Installierte **Komponenten:** im Dialogfeld COM-Wrapper die Option "Active DS Type Library" (Aktive DS-Typbibliothek) aus. Wenn die Typbibliothek nicht im Listenfeld angezeigt wird, klicken Sie auf die **Schaltfläche Durchsuchen...** , navigieren Sie zu dem Verzeichnis, in dem Activeds.tlb gespeichert ist, und wählen Sie dann die Typbibliothek aus.

Visual J++ erstellt das activeds-Paket für die Java Wrapper-Klassen und enthält das Paket in den Standardpfad des Projekts. Weitere Informationen finden Sie im ActiveDs-Paket im Project **Visual** J++-Fenster im Bereich Untersuchen.

Um ein ADSI-Objekt zu erhalten, das nicht kocreated werden kann, verwenden Sie eine der verfügbar gemachten ADSI-API-Funktionen, z. B. [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), die ebenfalls in Activeds.dll. Microsoft J/Direct bietet Zugriff auf diese und andere native APIs. Dies wird in den letzten beiden Zeilen des obigen Codebeispiels veranschaulicht.

Stellen Sie beim Kompilieren sicher, dass die Microsoft-Spracherweiterung aktiviert ist. Wählen Sie dazu im Visual **J++-Projektfenster** Project **&lt; &gt; Projekteigenschaften...** aus. Klicken Sie dann im **Dialogfeld Projekteigenschaften** auf **&lt; die Registerkarte &gt; Kompilieren.** Deaktivieren Sie **das Kontrollkästchen Microsoft-Spracherweiterungen** deaktivieren. Verwenden Sie beim Kompilieren über die Befehlszeile den Schalter "/x-", z. B.:

**jvc /x- SimpleADSI.java**

Damit der virtuelle Computer schließlich die COM-Komponente laden kann, muss die Dynamic Link Library (DLL) im Systempfad sichtbar sein. Wenn der Fehler "java.lang.UnsatisfiedLinkError" zurückgegeben wird, legen Sie PATH so fest, dass er den Pfad enthält, der die erforderliche DLL enthält. Wenn beispielsweise Activeds.dll in c: adsi lib installiert wurde, geben Sie den \\ folgenden Befehl über die Befehlszeile \\ aus:

**set PATH = %PATH%; c: \\ adsi \\ lib**

 

 




