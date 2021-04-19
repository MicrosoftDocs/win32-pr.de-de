---
description: Ein asynchroner Befehl zum Ausführen des Diagramms ist fehlgeschlagen.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356346"
---
# <a name="ec_error_stillplaying"></a>EC- \_ Fehler \_ beim Stillen

Ein asynchroner Befehl zum Ausführen des Diagramms ist fehlgeschlagen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter Graph-Manager einen asynchronen Run-Befehl ausgibt, der fehlschlägt, sendet er dieses Ereignis an die Anwendung. Das Diagramm verbleibt im Status "wird ausgeführt". Der Status der zugrunde liegenden Filter ist unbestimmt. Möglicherweise werden einige Filter ausgeführt, andere hingegen nicht.

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

 

 




