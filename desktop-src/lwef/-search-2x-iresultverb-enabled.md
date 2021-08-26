---
title: IResultVerb Enabled-Eigenschaft (WdsSharedIDL.h)
description: Diese Eigenschaft gibt TRUE zurück, wenn das Verb aktiviert ist.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Aktivierte Eigenschaft Legacy Windows Umgebungsfeatures
- Aktivierte Eigenschaft Legacy Windows Umgebungsfeatures, IResultVerb-Schnittstelle
- IResultVerb-Schnittstelle Legacy Windows Environment Features , Enabled (Eigenschaft)
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96a4c40252bf6b5ab74d3d4ec96e2568dffeed624ae2b5126059192dd72d9e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014320"
---
# <a name="iresultverbenabled-property"></a>IResultVerb::Enabled-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Diese Eigenschaft gibt TRUE zurück, wenn das Verb aktiviert ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft gibt True zurück, wenn das Verb aktiviert ist, oder False, wenn dies nicht der Fall ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





