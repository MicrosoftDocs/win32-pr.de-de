---
description: Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Erstellen von lokalisierten Klassendefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351854"
---
# <a name="creating-localized-class-definitions"></a>Erstellen von lokalisierten Klassendefinitionen

Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess. Sie beginnen mit dem Schreiben von MOF-Code, der die Klassen definiert, einschließlich aller Qualifizierer, die lokalisiert werden müssen. Diese ursprüngliche Datei wird als "Master MOF"-Datei bezeichnet, da Sie alle Qualifizierer und Eigenschaften enthält, die die Klasse definieren.

Verwenden Sie als nächstes den [MOF-Compiler](mofcomp.md) , um die sprach neutralen und sprachspezifischen Versionen der MOF-Datei zu erstellen. Der MOF-Compiler platziert die grundlegende Klassen Beschreibung in einer neuen MOF-Datei und erstellt eine lokalisierte Version der MOF-Datei, die nur die Eigenschaften und Qualifizierer enthält, die lokalisiert werden müssen. Obwohl die sprachspezifischen und sprach neutralen Versionen der MOF-Datei den gleichen Dateinamen haben können, sollten Sie eine MFL-Dateinamenerweiterung verwenden, um anzugeben, dass die Datei lokalisierte Informationen enthält. Sie können die MFL-Datei ggf. mit anderen Gebiets Schemata lokalisieren. Zum Speichern der Klassendefinitionen im CIM-Repository ist ein zusätzlicher Schritt erforderlich, um den MOF-Compiler zum Kompilieren der sprach neutralen und sprachspezifischen MOF-Dateien zu verwenden.

In den folgenden Schritten wird beschrieben, wie eine lokalisierte Klassendefinition erstellt und gespeichert wird.

**So erstellen und speichern Sie eine lokalisierte Klassendefinition**

1.  Erstellen Sie die MOF-Master Datei, mit der die Klassen definiert werden, die lokalisiert werden sollen.

    Speichern Sie diesen MOF-Code in einer Datei namens mastermof. mof.

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  Erstellen Sie sprachneutrale und sprachspezifische Versionen der MOF-Datei, indem Sie die mastermof. MOF-Datei kompilieren.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die Datei mastermof. MOF zu kompilieren.

    **"MOF": "MOF-MFL: lsmof. MFL-Zusatz: ms \_ 409 mastermof. mof"**

3.  Kompilieren Sie die sprach neutralen (lnmof. MOF) und sprachspezifischen Dateien (lsmof. MFL), und speichern Sie die Klassen Informationen im CIM-Repository.

    Geben Sie die folgenden Befehle an einer Eingabeaufforderung ein, um die Klassen Informationen im CIM-Repository zu speichern.

    **"Mamacomp lnmof. mof"**

    **"Mumacomp lsmof. MFL"**

    Nachdem Sie diese Dateien kompiliert haben, verfügen Sie über eine sprachneutrale Klassendefinition im Stamm \\ Test Namespace und eine lokalisierte Klassendefinition im Stamm \\ Test \\ MS 409- \_ Namespace. Weitere Informationen zum Kompilieren lokalisierter MOF-Dateien finden Sie unter [Kompilieren lokalisierter MOF-Dateien](compiling-localized-mof-files.md).

 

 



