---
description: In einem Stream ist ein Fehler aufgetreten, aber der Stream wird weiterhin wiedergegeben.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf78f1fba25316155e36eef1ed469a32bba1ce7c194a6dffb200f1fce5ede3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819997"
---
# <a name="ec_stream_error_stillplaying"></a>EC \_ STREAM \_ ERROR \_ STILLPLAYING

In einem Stream ist ein Fehler aufgetreten, aber der Stream wird weiterhin wiedergegeben.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Fehlercode des fehlgeschlagenen Vorgangs.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Kleiner Fehlercode. Dieser Wert ist in der Regel 0 (null).

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine. Die Anwendung muss entscheiden, ob das Diagramm beendet werden soll.

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

 

 




