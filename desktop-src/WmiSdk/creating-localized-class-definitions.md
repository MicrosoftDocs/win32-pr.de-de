---
description: Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Erstellen lokalisierter Klassendefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d7cb5f2970c3696de7cdd1bdb9d61d6eed5e86dc60c8941eec475d15145dd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374770"
---
# <a name="creating-localized-class-definitions"></a>Erstellen lokalisierter Klassendefinitionen

Das Erstellen lokalisierter Klassendefinitionen ist ein dreistufiger Prozess. Zunächst schreiben Sie MOF-Code, der die Klassen definiert, einschließlich aller Qualifizierer, die lokalisiert werden müssen. Diese ursprüngliche Datei wird als MOF-Masterdatei bezeichnet, da sie alle Qualifizierer und Eigenschaften enthält, die die Klasse definieren.

Verwenden Sie als Nächstes den [MOF-Compiler,](mofcomp.md) um die sprachneutralen und sprachspezifischen Versionen der MOF-Datei zu erstellen. Der MOF-Compiler platziert die grundlegende Klassenbeschreibung in einer neuen MOF-Datei und erstellt eine lokalisierte Version der MOF-Datei, die nur die Eigenschaften und Qualifizierer enthält, die lokalisiert werden müssen. Obwohl die sprachspezifischen und sprachneutralen Versionen der MOF-Datei den gleichen Dateinamen aufweisen können, sollten Sie eine MFL-Dateinamenerweiterung verwenden, um anzugeben, dass die Datei lokalisierte Informationen enthält. Sie können die MFL-Datei bei Bedarf in andere Gebietsschemas lokalisieren. Das Speichern der Klassendefinitionen im CIM-Repository erfordert einen zusätzlichen Schritt der Verwendung des MOF-Compilers, um sowohl die sprachneutralen als auch die sprachspezifischen MOF-Dateien zu kompilieren.

In den folgenden Schritten wird beschrieben, wie Sie eine lokalisierte Klassendefinition erstellen und speichern.

**So erstellen und speichern Sie eine lokalisierte Klassendefinition**

1.  Erstellen Sie die MOF-Masterdatei, die die Klassen definiert, die lokalisiert werden sollen.

    Speichern Sie diesen MOF-Code in einer Datei namens Mastermof.mof.

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

2.  Erstellen Sie sprachneutrale und sprachspezifische Versionen der MOF-Datei, indem Sie die Datei MasterMOF.mof kompilieren.

    Geben Sie den folgenden Befehl an einer Eingabeaufforderung ein, um die Datei MasterMOF.mof zu kompilieren.

    **mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

3.  Kompilieren Sie die sprachneutralen Dateien (Lnmof.mof) und die sprachspezifischen Dateien (Lsmof.mfl), und speichern Sie die Klasseninformationen im CIM-Repository.

    Geben Sie die folgenden Befehle an einer Eingabeaufforderung ein, um die Klasseninformationen im CIM-Repository zu speichern.

    **Mofcomp Lnmof.mof**

    **Mofcomp Lsmof.mfl**

    Nachdem Sie diese Dateien kompiliert haben, verfügen Sie über eine sprachneutrale Klassendefinition im \\ Stammtestnamespace und eine lokalisierte Klassendefinition im \\ \\ Stammtestnamespace ms \_ 409. Weitere Informationen zum Kompilieren lokalisierter MOF-Dateien finden Sie unter [Kompilieren lokalisierter MOF-Dateien.](compiling-localized-mof-files.md)

 

 



