---
title: Ribbon. HelpButton (Eigenschaft)
description: Stellt einen Container für die Hilfe Schaltfläche dar.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Menüband. HelpButton-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742296"
---
# <a name="ribbonhelpbutton-property"></a>Ribbon. HelpButton (Eigenschaft)

Stellt einen Container für die [Hilfe Schaltfläche](windowsribbon-controls-helpbutton.md)dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                           | BESCHREIBUNG                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup veranschaulicht, das zum Implementieren einer Menüband-Hilfe Schaltfläche erforderlich ist.

In diesem Code Abschnitt wird die Befehls Deklaration **Ribbon. HelpButton** angezeigt.


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



In diesem Code Abschnitt wird die Deklaration des **Ribbon. HelpButton** -Steuer Elements angezeigt.


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





