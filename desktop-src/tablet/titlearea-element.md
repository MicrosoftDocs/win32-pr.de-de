---
description: Enthält Speicherort und Begrenzungs Informationen für den Notiz Titel, falls vorhanden.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960763"
---
# <a name="titlearea-element"></a>TitleArea-Element

Enthält Speicherort und Begrenzungs Informationen für den Notiz Titel, falls vorhanden.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Titel**](title-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute



| Attribut  | type                      | Erforderlich | BESCHREIBUNG                                                                             | Mögliche Werte           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem äußersten äußersten linken Punkt im umgebenden Feld des Elements. | Eine beliebige ganze Zahl.              |
| **Top**    | **xs:integer**            | Erforderlich | Der Abstand zwischen dem Ursprung und dem obersten Punkt im umgebenden Feld für das Element.  | Eine beliebige ganze Zahl.              |
| **Width**  | **xs:nonNegativeInteger** | Erforderlich | Die Breite des Begrenzungs Rahmens für das Element.                                          | Eine beliebige nicht negative ganze Zahl. |
| **Height** | **xs:nonNegativeInteger** | Erforderlich | Die Höhe des umgebenden Felds für das Element.                                         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Elementtyp | ComplexType für [**titleareatype**](titleareatype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                      |
| Schemaname  | Journal Leser                                                  |



 

 

 



