---
title: Programmieren von ADSI mit Java/com
description: Mithilfe des Microsoft Virtual Machine for Java (Microsoft VM) und des Microsoft Java-Compilers haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programmieren von ADSI mit Java/com AD
- ADSI ADSI, using, Java/COM-Programmierung für
- ADSI ADSI, Beispielcode Java
- ADSI ADSI, Beispielcode-Java, binden an ein ADSI-Objekt und Aufrufen von Methoden für dieses Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855267"
---
# <a name="programming-adsi-with-javacom"></a>Programmieren von ADSI mit Java/com

Mithilfe des Microsoft Virtual Machine for Java (Microsoft VM) und des Microsoft Java-Compilers haben Sie Zugriff auf alle ADSI-Features, die über alle ADSI COM-Komponenten aus einer Java/COM-Anwendung verfügbar gemacht werden. Das folgende Java-Codebeispiel zeigt die Elemente, die zum Binden an ein ADSI-Objekt und zum Aufrufen von Methoden für dieses Objekt erforderlich sind. Die erforderlichen ADSI-API-Funktionen und-Objektmethoden werden über Activeds.dll verfügbar gemacht.


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



Das-Argument in der ersten **Import** Anweisung bezieht sich auf Java-Wrapper Klassen, die in Activeds.dll verpackt sind. Verwenden Sie Visual J++, um die Wrapper Klassen zu erstellen, und fügen Sie Sie in Ihr Projekt ein, indem Sie das folgende Verfahren ausführen.

**So erstellen Sie Wrapper Klassen und fügen Sie in Ihr Projekt ein**

1.  Wählen Sie in einem Visual J++-Projekt im Menü **Projekt** den Befehl **com-Wrapper hinzufügen...** aus.
2.  Wählen Sie "Active DS-Typbibliothek" aus den **installierten Komponenten aus:** im Dialogfeld COM-Wrapper. Wenn die Typbibliothek nicht im Listenfeld angezeigt wird, klicken Sie auf die Schaltfläche **Durchsuchen...** , navigieren Sie zu dem Verzeichnis, in dem activeds. tlb gespeichert ist, und wählen Sie dann die Typbibliothek aus.

Visual J++ erstellt das activeds-Paket für die Java-Wrapper Klassen und schließt das Paket in den Standardpfad des Projekts ein. Weitere Informationen finden Sie im activeds-Paket im Bereich " **Projekt durchsuchen** " im Fenster "Visual J++".

Um ein ADSI-Objekt zu erhalten, das nicht coerstellt werden kann, verwenden Sie eine der verfügbar gemachten ADSI-API-Funktionen, z. b. [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) oder [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), die ebenfalls in Activeds.dll verpackt sind. Microsoft J/Direct ermöglicht den Zugriff auf diese und andere Native APIs. Dies wird in den letzten beiden Zeilen des obigen Code Beispiels veranschaulicht.

Stellen Sie beim Kompilieren sicher, dass die Microsoft-Spracherweiterung aktiviert ist. Wählen Sie hierzu im Projektfenster von Visual J++ im Menü **Projekt** die Option **<project> Eigenschaften...** aus. Klicken Sie dann im Dialogfeld **<project> Eigenschaften** auf die Registerkarte **Kompilieren** . Deaktivieren Sie das Kontrollkästchen **Microsoft-Spracherweiterungen deaktivieren** . Wenn Sie in der Befehlszeile kompilieren, verwenden Sie den Schalter "/x-", z. b.:

**JVC/x-simpleadsi. Java**

Schließlich muss die Dynamic Link Library (dll) im Systempfad sichtbar sein, damit die virtuelle Maschine die COM-Komponente lädt. Wenn ein Fehler "java. lang. unbefriefedlinkerror" zurückgegeben wird, legen Sie den Pfad so fest, dass er den Pfad enthält, der die erforderliche DLL enthält. Wenn Activeds.dll z. b. in c: \\ ADSI lib installiert wurde \\ , geben Sie den folgenden Befehl über die Befehlszeile aus:

**set path =% path%; c: \\ ADSI \\ lib**

 

 




