---
title: IResultType DisplayName-Eigenschaft (WdsSharedIDL.h)
description: Lokalisierter Anzeigename des Typs
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- DisplayName-Eigenschaft Legacy Windows Umgebungsfeatures
- DisplayName-Eigenschaft Legacy Windows Environment Features , IResultType-Schnittstelle
- IResultType-Schnittstelle Legacy Windows Environment Features , DisplayName-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e045306250d2642ae281d81c8ffb8ab5a298134bf999ddba6abd5fd1660aeb1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399786"
---
# <a name="iresulttypedisplayname-property"></a>IResultType::D isplayName-Eigenschaft

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Lokalisierter Anzeigename des Typs:

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Eigenschaftswert

gibt die Adresse des lokalisierten Anzeigenamens für den Typ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





