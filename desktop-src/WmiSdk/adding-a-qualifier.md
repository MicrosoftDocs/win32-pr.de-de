---
description: Ein Qualifizierer ist eine Datenzeichenfolge, die weitere Informationen zu einer Klasse, Instanz, Eigenschaft, Methode oder einem Parameter bereitstellt.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Hinzufügen eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c24e89d711a8998c58c6201776d5d4c50cc1107f4c9ca4308d9cc992b44dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557823"
---
# <a name="adding-a-qualifier"></a>Hinzufügen eines Qualifizierers

Ein Qualifizierer ist eine Datenzeichenfolge, die weitere Informationen zu einer Klasse, Instanz, Eigenschaft, Methode oder einem Parameter bereitstellt.

Die folgende Klassendefinition ist ein Beispiel für eine abgeleitete Klasse mit Klassenqualifizierern.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Qualifizierer können in Standardqualifizierer, CIM-Qualifizierer und eindeutige Qualifizierer unterteilt werden:

-   Standardqualifizierer

    Ein Standardqualifizierer ist ein von WMI definierter Qualifizierer, der häufig in MOF-Code verwendet wird. Beispielsweise sind die [**Qualifizierer "Dynamisch"**](dynamic-qualifier.md) und [**"Lesen"**](standard-qualifiers.md) standardqualifizierer. Weitere Informationen finden Sie unter [WMI-Qualifizierer.](wmi-qualifiers.md)

-   CIM-Qualifizierer

    Ein CIM-Qualifizierer ist ein in der CIM-Spezifikation enthaltener Qualifizierer. Während CIM-Qualifizierer in MOF-Code verwendet werden, sind die Standardqualifizierer speziell unter Berücksichtigung von WMI konzipiert. Weitere Informationen finden Sie in der DMTF [CIM-Spezifikation.](https://www.dmtf.org/spec/cims.html/)

-   Eindeutiger Qualifizierer

    Ein eindeutiger Qualifizierer ist ein Qualifizierer, der von einem Klassenanbieter speziell für eine neue Klasse definiert wird. Der Units-Qualifizierer ist beispielsweise ein anbieterspezifischer Qualifizierer, der nicht dem Standard entspricht. [](standard-qualifiers.md) Sie können eigene Qualifizierer für die Verwendung mit Ihrem Anbieter erstellen. Weitere Informationen zum Erstellen eines Anbieters finden Sie unter [Entwickeln eines WMI-Anbieters.](developing-a-wmi-provider.md)

Unabhängig von Ihrem Qualifizierer besteht der Hauptprozess darin, den Qualifizierer in Ihrem MOF-Code zu verwenden. Weitere Informationen finden Sie unter [Anwenden eines Qualifizierers.](applying-a-qualifier.md) Sie können einen Qualifizierer mit einer Qualifizierer-Variante weiter beschreiben. Eine Qualifizierer-Variante enthält weitere Informationen dazu, wie ein Anbieter einen Qualifizierer verwenden soll. Weitere Informationen finden Sie unter [Beschreiben eines Qualifizierers mit einer Qualifizierer-Variante.](describing-a-qualifier-with-a-qualifier-flavor.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von MOF-Klassen (Managed Object Format)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



