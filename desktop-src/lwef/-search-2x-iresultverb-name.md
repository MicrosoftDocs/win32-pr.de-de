---
title: IResultVerb Name-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft gibt einen Zeiger auf den kononischen Namen für das Verb zurück, z. B. print, open usw.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Name der Eigenschaft Legacy Windows Umgebungsfeatures
- Name der Eigenschaft Legacy Windows Environment Features , IResultVerb interface
- IResultVerb-Schnittstelle Legacy Windows Environment Features , Name -Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e58377a9286a6e3fe4abb8d0a1d4ebf9e10bd3072295484ca32fb56d465a6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976970"
---
# <a name="iresultverbname-property"></a>IResultVerb::Name-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft gibt einen Zeiger auf den kononischen Namen für das Verb zurück, z. B. print, open usw.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

name ist ein Zeiger auf den kononischen Namen für das Verb.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





