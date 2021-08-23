---
description: Gibt den Zeitstempel für den letzten Frameschritt an.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4d3cc09d286f6955dda30aeb77288b75e90e8c66777a5f9f16246507f64b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686090"
---
# <a name="ec_scrub_time"></a>\_ \_ EC-REINIGUNGSZEIT

Gibt den Zeitstempel für den letzten Frameschritt an.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Niedrigere 32 Bits des Zeitstempels.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Obere 32 Bits des Zeitstempels.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Der Moderator für den EVR-Filter [**(Enhanced Video Renderer)**](enhanced-video-renderer-filter.md) sendet diese Nachricht an den EVR, wenn er einen Frameschritt abgeschlossen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> </dl>

 

 




