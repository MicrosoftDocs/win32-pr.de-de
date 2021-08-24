---
description: In einem Audiorendererfilter ist ein Gerätefehler aufgetreten.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefe6dbe57b26bf167a7fbc668010930bacffc321d42d2847ae6776696e009fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792410"
---
# <a name="ec_snddev_out_error"></a>EC \_ SNDDEV \_ OUT \_ ERROR

In einem Audiorendererfilter ist ein Gerätefehler aufgetreten.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

DWORD-Wert aus dem [**aufzählten SNDDEV \_ ERR-Typ,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) der angibt, wie auf das Gerät zugegriffen wurde, als der Fehler aufgetreten ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

DWORD-Wert, der den Vom Soundgeräteaufruf zurückgegebenen Fehler angibt.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

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

 

 




