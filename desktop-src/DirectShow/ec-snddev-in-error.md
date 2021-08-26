---
description: In einem Audioaufnahmefilter ist ein Gerätefehler aufgetreten.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfc65b751010288ed37fc1596e020887e6ea901c451dcdac729fe05ea33f93a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102810"
---
# <a name="ec_snddev_in_error"></a>EC \_ SNDDEV \_ IN \_ ERROR

In einem Audioaufnahmefilter ist ein Gerätefehler aufgetreten.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

DWORD-Wert aus dem [**SNDDEV-ERR-Enumerationstyp, \_**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) der angibt, wie auf das Gerät zugegriffen wurde, als der Fehler aufgetreten ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

DWORD-Wert, der den vom Soundgeräteaufruf zurückgegebenen Fehler angibt.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




