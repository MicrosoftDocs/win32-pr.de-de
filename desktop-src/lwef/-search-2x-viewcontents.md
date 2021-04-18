---
title: Viewcontents-Enumeration
description: Wird von iresultsviewer-Inhalten verwendet, um anzugeben, wie der aktuelle Abfrage Rückgabe Satz angezeigt wird, oder legt ihn fest.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Viewcontents-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364552"
---
# <a name="viewcontents-enumeration"></a>Viewcontents-Enumeration

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Wird von [**iresultsviewer:: Contents**](-search-2x-iresultsviewer-contents.md) verwendet, um anzugeben, wie die aktuelle Abfrage Rückgabe Menge angezeigt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**Ergebnis angezeigt**
</dt> <dd>

Gibt den Typ des Inhalts an, der in der Ergebnis Ansicht angezeigt wird.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**Shellviewanzeige**
</dt> <dd>

Gibt an, welcher Typ von Inhalt, der in der Ergebnis Ansicht angezeigt wird, derzeit auf die shellansicht festgelegt ist.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**Webbrowseranzeige**
</dt> <dd>

Gibt an, welcher Typ von Inhalt, der in der Ergebnis Ansicht angezeigt wird, derzeit auf die Browseransicht festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wdsview. idl</dt> </dl> |



 

 





