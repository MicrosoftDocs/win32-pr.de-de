---
description: Signalisiert, dass ein DVD-Datenträger in das Laufwerk eingefügt wurde.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6911d4ad044e0b2080007f9751bd7090b182d8474673da98d35dd91544947e03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997920"
---
# <a name="ec_dvd_disc_inserted"></a>\_ \_ EC-DVD-DATENTRÄGER \_ EINGEFÜGT

Signalisiert, dass ein DVD-Datenträger in das Laufwerk eingefügt wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Wiedergabe beginnt automatisch, wenn ein Datenträger eingefügt wird. Die Anwendung muss als Reaktion auf dieses Ereignis keine besonderen Maßnahmen ergreifen.

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




