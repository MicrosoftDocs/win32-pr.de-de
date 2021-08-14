---
title: IResultVerb DisplayName-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft gibt einen Zeiger auf den lokalisierten Anzeigenamen für das Verb zurück.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- DisplayName-Eigenschaft Legacy Windows-Umgebungsfeatures
- DisplayName-Eigenschaft Legacy Windows Umgebungsfeatures, IResultVerb-Schnittstelle
- IResultVerb-Schnittstelle Legacy Windows Umgebungsfeatures, DisplayName-Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d7f72d0d028fa6a6ecdede7f2d88e3e3dea0a37a14cc6365dc5da2d14992af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694718"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb::D isplayName-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft gibt einen Zeiger auf den lokalisierten Anzeigenamen für das Verb zurück.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft gibt einen Zeiger auf den lokalisierten Anzeigenamen für das Verb zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





