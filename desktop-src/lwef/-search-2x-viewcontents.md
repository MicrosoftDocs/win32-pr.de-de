---
title: ViewContents-Enumeration
description: Wird von IResultsViewer Contents verwendet, um anzugeben oder festzulegen, wie der aktuelle Abfragerückgabesatz angezeigt wird.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents-Enumeration– Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829110"
---
# <a name="viewcontents-enumeration"></a>ViewContents-Enumeration

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Wird von [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) verwendet, um anzugeben oder festzulegen, wie der aktuelle Abfragerückgabesatz angezeigt wird.

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

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

Gibt den Inhaltstyp an, der in der Ergebnisansicht angezeigt wird.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Gibt an, dass der Inhaltstyp, der in der Ergebnisansicht angezeigt wird, derzeit auf die Shellansicht festgelegt ist.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Gibt an, dass der Inhaltstyp, der in der Ergebnisansicht angezeigt wird, derzeit auf die Browseransicht festgelegt ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





