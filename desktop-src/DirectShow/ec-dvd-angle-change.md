---
description: Signalisiert, dass entweder die Anzahl der verfügbaren Winkel geändert wurde oder die aktuelle Winkel Zahl geändert wurde.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372657"
---
# <a name="ec_dvd_angle_change"></a>Änderung des EC- \_ DVD- \_ Winkels \_

Signalisiert, dass entweder die Anzahl der verfügbaren Winkel geändert wurde oder die aktuelle Winkel Zahl geändert wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die Anzahl der verfügbaren Winkel angibt. Wenn die Anzahl der verfügbaren Winkel 1 beträgt, ist das aktuelle Video nicht multiangle.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD** -Wert, der die aktuelle Winkel Zahl angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Winkel Zahlen reichen von 1 bis 9.

Die aktuelle Spitzen Zahl kann sich automatisch ändern, indem ein Navigations Befehl, der auf der Festplatte erstellt wurde, und die Anwendungssteuerung mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle erstellt wird.

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode. h (Include DShow. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




