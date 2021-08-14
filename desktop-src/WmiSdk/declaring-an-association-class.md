---
description: Eine Zuordnungsklasse ist ein spezieller Typ von Klasse, der eine Beziehung zwischen zwei anderen Klassen definiert.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Deklarieren einer Association-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd569d1dc20ba40be6d19f3009ab4311f69e04ca3e8a01031e74a9c84b461552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244420"
---
# <a name="declaring-an-association-class"></a>Deklarieren einer Association-Klasse

Eine Zuordnungsklasse ist ein spezieller Typ von Klasse, der eine Beziehung zwischen zwei anderen Klassen definiert.

Im folgenden Verfahren wird beschrieben, wie Sie eine Zuordnungsklasse mit MOF-Code erstellen.

**So erstellen Sie eine Zuordnungsklasse mit MOF-Code**

1.  Weisen Sie den Zuordnungsqualifizierer Ihrer Klasse zu. 

    Obwohl es möglich ist, eine Klasse mit Verweisen auf  Objekte oder Klassen zu erstellen, macht die Verwendung des Association-Qualifizierers nicht nur deutlich, dass ihre Klasse eine Zuordnungsklasse ist, sondern stellt als bewährte Methode sicher, dass Ihre Klasse vollständig als Zuordnungsklasse funktioniert.

2.  Erstellen Sie zwei Verweise innerhalb der -Klasse, die die beiden Objektinstanzen beschreiben, die Sie mithilfe des Ref-Typs **miteinander verknüpfen** möchten.

    Die Verweise binden die beiden Objekte in der Zuordnung, indem sie Pfade zu den -Objekten enthalten. Obwohl dies nicht erforderlich ist, verwenden Sie auch die Verweiseigenschaften als Schlüsseleigenschaften.

    Obwohl Sie vollqualifizierte oder namespace relative Verweise erstellen können, bietet WMI nur eingeschränkte Unterstützung für namespaceübergreifende Verweise. Insbesondere können nur statisch definierte Objekte über Namespacegrenzen hinweg aufeinander verweisen. Dynamisch unterstützte Objekte können nicht aufeinander verweisen.

    Verwenden Sie bei Bedarf die **HasClassRef-** und Classref-Qualifizierer in Verbindung mit dem **Objektverweistyp,** um auf eine Klasse zu verweisen. 

    WMI unterstützt, dass ein **Verweispunkt** auf eine Instanz und der andere **Objektverweispunkt** auf eine Klasse verwendet wird. In diesem Fall würde ihre Zuordnungsklasse eine Zuordnung beschreiben, die Instanzen an Klassen bindet.

    Im folgenden Codebeispiel wird die Syntax für die Verwendung von **HasClassRef** und **Classref mit** einem **Objekttyp** beschrieben.

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    Im vorherigen Beispiel kann der **ep1-Verweis** auf die Klassendefinitionen für die **MyEndpoint-Klasse** oder die **OtherContainer-Klasse** verweisen. Beachten Sie, dass Sie zwar die Verweisklasse schwach  eingeben müssen, den Classref-Qualifizierer selbst jedoch nicht schwach eingeben können. Dies würde die Effizienz der WMI-Abfrage-Engine erheblich reduzieren. Die schwache Typisierung erstellt einen Verweis, der  jeden Datentyp mithilfe des Object-Schlüsselworts und **des ref-Datentyps** enthalten kann. Um **HasClassRef erfolgreich verwenden zu** können, müssen Sie die relevanten Qualifizierer-Varianten so festlegen, dass sie an alle Instanzen und Unterklassen weiter geben.

3.  Erstellen Sie nach Bedarf weitere Eigenschaften.

    Das folgende Codebeispiel zeigt, dass WMI zuordnungsklassen mit weniger oder mehr als zwei Verweiseigenschaften derzeit nicht unterstützt.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Kompilieren Sie ihren MOF-Code mit dem MOF-Compiler, wenn Sie fertig sind.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Im Codebeispiel in Schritt 3 wird die **Zuordnungsklasse MyAssocClass** definiert. Die **MyAssocClass-Klasse** definiert eine Beziehung zwischen **ClassX** und **ClassY.** Die **Eigenschaften PathToClassX** und **PathToClassY** enthalten Objektpfade zu den Instanzen der klassen, die zugeordnet werden sollen. Das Schlüsselwort **ToInstance ist** eines von mehreren Flavor-Flags, die WMI definiert, um Informationen zur Verwendung eines Qualifizierers zu liefern. Das **ToInstance-Schlüsselwort** gibt an, dass WMI den Zuordnungsqualifizierer an alle Instanzen der Zuordnungsklasse weitergibt.  Durch Überprüfen dieses Instanzqualifizierers kann die Clientsoftware feststellen, dass eine Instanz zu einer Zuordnungsklasse gehört, ohne die Klassendefinition abrufen zu müssen, um nach dem Zuordnungsqualifizierer zu suchen.  Weitere Informationen finden Sie unter [Beschreiben eines Qualifizierers mit einer Qualifizierer-Variante und](describing-a-qualifier-with-a-qualifier-flavor.md) [Verweisen.](references.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen Managed Object Format -Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



