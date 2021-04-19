---
description: Gibt die Zeitspanne an, die eine Komponente zum Verarbeiten der einzelnen Stichproben einnimmt.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353792"
---
# <a name="ec_processing_latency"></a>EC- \_ Verarbeitungs \_ Latenz

Gibt die Zeitspanne an, die eine Komponente zum Verarbeiten der einzelnen Stichproben einnimmt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(Konstante **Referenz \_ Zeit** \* ) die Zeitspanne für die Verarbeitung der einzelnen Stichproben in 100-Nanosecond-Einheiten.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Ein Präsentator für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR) kann diese Nachricht an den EVR senden, um den EVR über die Verarbeitungs Wartezeit des Presenter zu benachrichtigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




