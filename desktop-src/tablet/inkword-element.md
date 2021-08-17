---
description: Enthält Informationen zu einem bestimmten Ink-Wort in der Journalnotiz, einschließlich Position, Alternativen und der tatsächlichen Ink-Daten.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342da6688088d37065af7af8600ac2e1e7003599914b320b21e49d39235dc712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717319"
---
# <a name="inkword-element"></a>InkWord-Element

Enthält Informationen zu einem bestimmten Ink-Wort in der Journalnotiz, einschließlich Position, Alternativen und der tatsächlichen Ink-Daten.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**GroupNode**](groupnode-element.md)

[**Linie**](line-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Confidence**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attribute



| attribute  | type                      | Erforderlich | Beschreibung                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten linken Punkt im Begrenzungsfeld für das Element. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im Begrenzungsfeld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungsfelds für das Element.                                          | Eine nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des Begrenzungsfelds für das Element.                                         | Eine nicht negative ganze Zahl. |



 

> [!WARNING]
> Die interne Koordinatenzuordnung des Ink-Worts ist Englische Metrikeinheiten, und ein Multiplikator von 2,54 muss von Ihrer Anwendung verwendet werden, um die Werte für Breite und Höhe in die HIMETRIC-Einheiten zu konvertieren, die von den Tablet PC-Plattform-APIs verwendet werden.

 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|-------------------------------------------------------------|
| Elementtyp | [**ComplexType: InkWordType**](inkwordtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Schemaname  | Journalreader                                              |



 

 

 



