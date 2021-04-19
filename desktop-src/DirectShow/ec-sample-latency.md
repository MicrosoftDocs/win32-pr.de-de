---
description: Gibt an, wie weit hinter dem Zeitplan eine Komponente für die Verarbeitung von Beispielen liegt.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357313"
---
# <a name="ec_sample_latency"></a>Wartezeit für EC- \_ Beispiel \_

Gibt an, wie weit hinter dem Zeitplan eine Komponente für die Verarbeitung von Beispielen liegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(Konstante **Referenz \_ Zeit** \* ), die sich hinter der Komponente befindet, in 100-Nanosecond-Einheiten. Wenn dieser Wert positiv ist, befindet sich die Komponente hinter dem Zeitplan. Wenn dieser Wert negativ ist, liegt die Komponente vor dem Zeitplan.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Ein benutzerdefinierter Presenter für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR) kann diese Nachricht an den EVR senden, um den EVR zu benachrichtigen, ob der Presenter hinter einem Zeitplan oder vor dem Zeitplan steht.

Die einfachste Möglichkeit zum Berechnen *von lParam1* ist: *QPC now*   *QPC Target*, wobei *QPC jetzt* die Uhrzeit und *QPC Target* die Präsentationszeit ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Schreiben von EVR Presenter](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

