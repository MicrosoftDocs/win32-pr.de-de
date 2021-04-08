---
description: Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: MessageType-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960433"
---
# <a name="messagetypedeclarations-element"></a>MessageType-Deklarations Element

Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.

## <a name="usage"></a>Verbrauch

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>  |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Auf Schema Tabellen wird durch Porttyp Definitionen verwiesen. Dieses Element wird daher in der Regel direkt vor [**porttypeer Definitions**](porttypedefinitions.md) Elementen verwendet.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




