---
description: Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: messageTypeDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a94fabdd2ceb2d32052a692f6daa1abba0a52f16d5d1b7dd0a4cef07d33de09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757080"
---
# <a name="messagetypedefinitions-element"></a>messageTypeDefinitions-Element

Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.

## <a name="usage"></a>Verbrauch

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | Beschreibung                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**Vorgang**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>  |
| [**Porttype**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die von [**messageTypeDeclarations deklarierten Schematabellen**](messagetypedeclarations.md)bereitzustellen.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




