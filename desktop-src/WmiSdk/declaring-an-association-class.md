---
description: Eine Association-Klasse ist eine besondere Art von Klasse, die eine Beziehung zwischen zwei anderen Klassen definiert.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Deklarieren einer Association-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050268"
---
# <a name="declaring-an-association-class"></a>Deklarieren einer Association-Klasse

Eine Association-Klasse ist eine besondere Art von Klasse, die eine Beziehung zwischen zwei anderen Klassen definiert.

Im folgenden Verfahren wird beschrieben, wie eine Association-Klasse mithilfe von MOF-Code erstellt wird.

**So erstellen Sie eine Association-Klasse mithilfe von MOF-Code**

1.  Weisen Sie der Klasse den **Association** -Qualifizierer zu.

    Obwohl es möglich ist, eine Klasse mit Verweisen auf Objekte oder Klassen zu erstellen, wird durch die Verwendung des **Association** -Qualifizierers nicht nur klar, dass es sich bei der Klasse um eine Association-Klasse handelt, sondern es wird als bewährte Vorgehensweise sichergestellt, dass die Klasse vollständig als Zuordnungs Klasse fungiert.

2.  Erstellen Sie zwei Verweise innerhalb der-Klasse, die die beiden Objektinstanzen beschreiben, die Sie mit dem **ref** -Typ verknüpfen möchten.

    Die Verweise binden die beiden Objekte in der Zuordnung, indem Sie die Pfade zu den-Objekten enthalten. Auch wenn dies nicht erforderlich ist, verwenden Sie die Verweis Eigenschaften als Schlüsseleigenschaften.

    Obwohl Sie vollständig qualifizierte Verweise oder Namespace relative Verweise erstellen können, bietet WMI nur eingeschränkte Unterstützung für Namespace übergreifende Verweise. Insbesondere können nur statisch definierte Objekte über Namespace Grenzen hinweg referenziert werden. dynamisch unterstützte Objekte können nicht aufeinander verweisen.

    Verwenden Sie ggf. die Qualifizierer **hasclassref** und **classref** in Verbindung mit dem **Objekt** Verweistyp, um auf eine Klasse zu verweisen.

    WMI unterstützt das **vorhanden sein eines** Verweis Verweises auf eine Instanz, und der andere **Objekt** Verweis verweist auf eine Klasse. In diesem Fall würde ihre Association-Klasse eine Zuordnung beschreiben, die Instanzen an Klassen bindet.

    Im folgenden Codebeispiel wird die Syntax für die Verwendung von **hasclassref** und **classref** mit einem **Objekttyp** beschrieben.

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    Im vorherigen Beispiel kann der **EP1** -Verweis auf die Klassendefinitionen für die **myEndpoint** -Klasse oder die **othercontainer** -Klasse verweisen. Beachten Sie, dass Sie zwar die Verweis Klasse schwach eingeben müssen, Sie können den **classref** -Qualifizierer selbst jedoch nicht schwach eingeben. Dadurch würde die Effizienz der WMI-Abfrage-Engine erheblich reduziert werden. Schwache Typisierung ist das Erstellen eines Verweises, der beliebige Datentypen enthalten kann, indem das **Object** **-Schlüssel** Wort und der Verweis Datentyp verwendet werden Damit **hasclassref** erfolgreich verwendet werden kann, müssen Sie die relevanten qualifizierervarianten so festlegen, dass Sie an alle Instanzen und Unterklassen weitergegeben werden.

3.  Erstellen Sie ggf. weitere Eigenschaften.

    Das folgende Codebeispiel zeigt, dass WMI derzeit keine Zuordnungs Klassen unterstützt, die über weniger oder mehr als zwei Verweis Eigenschaften verfügen.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Wenn Sie fertig sind, kompilieren Sie den MOF-Code mit dem MOF-Compiler.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Das Codebeispiel in Schritt 3 definiert die Klasse **myassocclass** Association. Die **myassocclass** -Klasse definiert eine Beziehung zwischen **ClassX** und **eleganten**. Die Eigenschaften **pathyclassx** und **pathyedle** enthalten Objekt Pfade zu den Instanzen der Klassen, die zugeordnet werden sollen. Das Schlüsselwort " **deinstance** " ist eines von mehreren Standardflags, die von WMI definiert werden, um Informationen zur Verwendung eines Qualifizierers bereitzustellen. Das Schlüsselwort " **deinstance** " gibt an, dass WMI den **Assoziations** Qualifizierer an alle Instanzen der Association-Klasse weitergeben soll. Durch die Überprüfung dieses instanzqualifizierers kann die Client Software ermitteln, dass eine Instanz zu einer Zuordnungs Klasse gehört, **ohne die Klassen** Definition abrufen zu müssen, um nach dem Zuordnungs Qualifizierer zu suchen. Weitere Informationen finden Sie unter [beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration](describing-a-qualifier-with-a-qualifier-flavor.md) und [verweisen](references.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



