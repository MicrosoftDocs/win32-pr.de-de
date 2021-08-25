---
description: Gibt die Zeit an, die eine Komponente zum Verarbeiten der einzelnen Stichproben in Bearbeitung nimmt.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb107dd4c895f9819d268e6112c22c0c514e480bf778692f28bc87853aee9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792620"
---
# <a name="ec_processing_latency"></a>\_ \_ EC-VERARBEITUNGSLATENZ

Gibt die Zeit an, die eine Komponente zum Verarbeiten der einzelnen Stichproben in Bearbeitung nimmt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME**) Die Zeit für die Verarbeitung der einzelnen Stichproben \* in Einheiten von 100 Nanosekunden.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Ein Moderator für den EVR-Filter [**(Enhanced Video Renderer)**](enhanced-video-renderer-filter.md) kann diese Nachricht an den EVR senden, um den EVR über die Verarbeitungslatenz des Moderators zu benachrichtigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




