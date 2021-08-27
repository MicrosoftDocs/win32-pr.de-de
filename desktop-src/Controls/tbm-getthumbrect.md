---
title: TBM_GETTHUMBRECT Meldung (Commctrl.h)
description: Ruft die Größe und Position des umschließenden Rechtecks für den Schieberegler in einer Trackleiste ab.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d2582ccfb5276f65cbf1187458774622e62f6dd87d8dcadd2e16a7447f769a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046360"
---
# <a name="tbm_getthumbrect-message"></a>TBM \_ GETTHUMBRECT-Nachricht

Ruft die Größe und Position des umschließenden Rechtecks für den Schieberegler in einer Trackleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur.**](/previous-versions//dd162897(v=vs.85)) Die Nachricht füllt diese Struktur mit dem umschließenden Rechteck des Schiebereglers der Trackleiste in Clientkoordinaten des Fensters der Trackleiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

