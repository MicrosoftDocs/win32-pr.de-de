---
title: Iresultproperty-Hinweis Eigenschaft (wdssharedidl. h)
description: Spezieller Wert, der für das Abrufen von Daten verwendet wird.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Hinweis Eigenschaft Legacy-Windows-Umgebungs Features
- Hinweis Eigenschaft Legacy-Windows-Umgebungs Features, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, Hint-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339956"
---
# <a name="iresultpropertyhint-property"></a>Iresultproperty:: Hint-Eigenschaft

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Spezieller Wert, der für das Abrufen von Daten verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt einen Zeiger auf den Hinweis zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

 





