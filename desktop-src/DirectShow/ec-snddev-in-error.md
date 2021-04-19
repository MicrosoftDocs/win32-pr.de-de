---
description: Ein Gerätefehler ist in einem audioerfassungs Filter aufgetreten.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352092"
---
# <a name="ec_snddev_in_error"></a>\_Fehler bei EC snddev. \_ \_

Ein Gerätefehler ist in einem audioerfassungs Filter aufgetreten.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

DWORD-Wert aus dem " [**snddev \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) "-enumerierten Typ, der angibt, wie auf das Gerät zugegriffen wurde, als der Fehler aufgetreten ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

DWORD-Wert, der den Fehler angibt, der vom Sound-Geräte Rückruf zurückgegeben wurde

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

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

 

 




