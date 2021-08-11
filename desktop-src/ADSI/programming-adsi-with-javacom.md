---
title: Programmieren von ADSI mit Java/COM
description: Mit dem virtuellen Microsoft-Computer für Java (Microsoft-VM) und dem Microsoft Java Compiler haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten verfügbar gemacht werden, aus einer Java/COM-Anwendung.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmieren von ADSI mit Java/COM AD
- ADSI ADSI , mit, Java/COM-Programmierung für
- ADSI ADSI , Beispielcode Java
- ADSI ADSI , Beispielcode Java , Bindung an ein ADSI-Objekt und Aufrufen von Methoden für dieses Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4778d1d1f71920f880fe38a71874283f7cd8628ae0376b3f9ce227305ab184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178974"
---
# <a name="programming-adsi-with-javacom"></a>Programmieren von ADSI mit Java/COM

Mit dem virtuellen Microsoft-Computer für Java (Microsoft-VM) und dem Microsoft Java Compiler haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten verfügbar gemacht werden, aus einer Java/COM-Anwendung. Das folgende Java-Codebeispiel zeigt die Elemente, die zum Binden an ein ADSI-Objekt und zum Aufrufen von Methoden für dieses Objekt erforderlich sind. Die erforderlichen ADSI-API-Funktionen und Objektmethoden werden über Activeds.dll verfügbar gemacht.


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



Das Argument in der ersten **import-Anweisung** bezieht sich auf Java Wrapper-Klassen, die in Activeds.dll gepackt sind. Verwenden Sie Visual J++, um die Wrapperklassen zu erstellen und in Ihr Projekt einzuschließen. Befolgen Sie dazu das folgende Verfahren.

**So erstellen Sie Wrapperklassen und schließen sie in Ihr Projekt ein**

1.  Wählen Sie in einem Visual J++-Projekt im **Menü Project** Com **Wrapper hinzufügen...** aus.
2.  Wählen Sie im Dialogfeld **Installierte Komponenten:** im Dialogfeld COM-Wrapper die Option "Active DS Type Library" (Aktive DS-Typbibliothek) aus. Wenn die Typbibliothek nicht im Listenfeld angezeigt wird, klicken Sie auf die Schaltfläche **Durchsuchen...,** navigieren Sie zu dem Verzeichnis, in dem Activeds.tlb gespeichert ist, und wählen Sie dann die Typbibliothek aus.

Visual J++ erstellt das Activeds-Paket für die Java Wrapper-Klassen und schließt das Paket in den Standardpfad des Projekts ein. Weitere Informationen finden Sie im ActiveDs-Paket im **Bereich "Project Durchsuchen"** im Visual J++-Fenster.

Um ein ADSI-Objekt abzurufen, das nicht cocreated werden kann, verwenden Sie eine der verfügbar gemachten ADSI-API-Funktionen, z. B. [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) oder [**ADsOpenObject,**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)die ebenfalls in Activeds.dll gepackt sind. Microsoft J/Direct bietet Zugriff auf diese und andere native APIs. Dies wird in den letzten beiden Zeilen des obigen Codebeispiels veranschaulicht.

Stellen Sie beim Kompilieren sicher, dass die Microsoft-Spracherweiterung aktiviert ist. Wählen Sie hierzu im Visual J++-Projektfenster im **Menü Project** **<project> eigenschaften...** aus. Klicken Sie dann im Dialogfeld **<project> Eigenschaften** auf die Registerkarte **Kompilieren.** Deaktivieren Sie das **Kontrollkästchen Microsoft-Spracherweiterungen deaktivieren.** Verwenden Sie beim Kompilieren über die Befehlszeile den Schalter "/x-", z. B.:

**jvc /x- SimpleADSI.java**

Damit der virtuelle Computer die COM-Komponente laden kann, muss die Dynamic Link Library (DLL) im Systempfad sichtbar sein. Wenn der Fehler "java.lang.UnsatisfiedLinkError" zurückgegeben wird, legen Sie path so fest, dass er den Pfad enthält, der die erforderliche DLL enthält. Wenn beispielsweise Activeds.dll in c: adsi lib installiert wurde, können Sie \\ den folgenden Befehl über die Befehlszeile \\ ausführen:

**set PATH = %PATH%; c: \\ adsi \\ lib**

 

 




