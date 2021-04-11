---
title: DTM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird. Senden Sie diese Nachricht explizit oder mithilfe des "DateTime \_ getidealsize"-Makros.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Windows-Steuerelemente für DTM_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213708"
---
# <a name="dtm_getidealsize-message"></a>DTM- \_ getidealsize-Nachricht

Ruft die Größe ab, die zum Anzeigen des Steuer Elements ohne Clipping benötigt wird. Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) "-Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet. Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die ideale Größe erhält. Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

