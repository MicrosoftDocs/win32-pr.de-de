---
description: Ein Qualifizierer ist eine Daten Zeichenfolge, die weitere Informationen über eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Parameter bereitstellt.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Fügen eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355466"
---
# <a name="adding-a-qualifier"></a>Fügen eines Qualifizierers

Ein Qualifizierer ist eine Daten Zeichenfolge, die weitere Informationen über eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Parameter bereitstellt.

Die folgende Klassendefinition ist ein Beispiel für eine abgeleitete Klasse mit Klassen Qualifizierern.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Qualifizierer können in Standard Qualifizierer, CIM-Qualifizierer und eindeutige Qualifizierer unterteilt werden:

-   Standard Qualifizierer

    Ein Standard Qualifizierer ist ein von WMI definierter Qualifizierer, der häufig in MOF-Code verwendet wird. Beispielsweise sind die Qualifizierer " [**Dynamic**](dynamic-qualifier.md) " und " [**Read**](standard-qualifiers.md) " Standard Qualifizierer. Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md).

-   CIM Qualifizierer

    Ein CIM-Qualifizierer ist ein Qualifizierer in der CIM-Spezifikation. Während Sie CIM-Qualifizierer in MOF-Code verwenden, sind die Standard Qualifizierer speziell auf WMI zugeschnitten. Weitere Informationen finden Sie in der DMTF [CIM-Spezifikation](https://www.dmtf.org/spec/cims.html/).

-   Eindeutige Qualifizierer

    Ein eindeutiger Qualifizierer ist ein Qualifizierer, der speziell für eine neue Klasse durch einen Klassen Anbieter definiert ist Der [**Einheiten**](standard-qualifiers.md) Qualifizierer ist beispielsweise ein nicht standardmäßiger Anbieter spezifischer Qualifizierer. Sie können Ihre eigenen Qualifizierer für die Verwendung mit Ihrem Anbieter erstellen. Weitere Informationen zum Erstellen eines Anbieters finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).

Was Ihr Qualifizierer tut, der Hauptprozess, den Sie ausführen, ist die Verwendung des Qualifizierers in Ihrem MOF-Code. Weitere Informationen finden Sie unter [Anwenden eines Qualifizierers](applying-a-qualifier.md). Sie können einen Qualifizierer mit einer qualifiziererkonfiguration weiter beschreiben. Eine qualifiziererkonfiguration enthält weitere Informationen zur Verwendung eines Qualifizierers durch einen Anbieter. Weitere Informationen finden Sie unter [beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



