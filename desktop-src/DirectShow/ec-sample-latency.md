---
description: Gibt an, wie weit der Zeitplan einer Komponente für die Verarbeitung von Beispielen zurück liegt.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686150"
---
# <a name="ec_sample_latency"></a>EC \_ SAMPLE \_ LATENCY

Gibt an, wie weit der Zeitplan einer Komponente für die Verarbeitung von Beispielen zurück liegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME** \* ) Der Abstand hinter der Komponente in Einheiten von 100 Nanosekunden. Wenn dieser Wert positiv ist, liegt die Komponente hinter dem Zeitplan. Wenn dieser Wert negativ ist, liegt die Komponente dem Zeitplan voraus.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Moderatorin für den FILTER [**"Enhanced Video Renderer"**](enhanced-video-renderer-filter.md) (EVR) kann diese Nachricht an die EVR senden, um den EVR zu benachrichtigen, ob der Moderator einen Zeitplan zurücklässt oder vor dem Zeitplan liegt.

Die einfachste Möglichkeit zum Berechnen von *lParam1* ist: *QPC* jetzt *QPC-Ziel,* wobei *QPC* jetzt die Uhrzeit und *QPC-Ziel* die Präsentationszeit ist.   

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Schreiben eines EVR-Presenters](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

