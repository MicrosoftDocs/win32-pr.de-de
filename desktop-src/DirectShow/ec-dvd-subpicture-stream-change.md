---
description: Signalisiert, dass die aktuelle Teilbild-streamnummer für den Haupttitel geändert wurde.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359305"
---
# <a name="ec_dvd_subpicture_stream_change"></a>Datenstrom Änderung des EC-DVD- \_ \_ subbildes \_ \_

Signalisiert, dass die aktuelle Teilbild-streamnummer für den Haupttitel geändert wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die neue Datenstrom Nummer des Benutzer Bilds angibt. Die Werte des subbildstreams reichen von 0 bis 31. Der Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Boolescher Wert, der den Zustand "ein/aus" des Teil Bilds angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Teilbild kann automatisch geändert werden, wenn ein Navigations Befehl auf der Festplatte und über die Anwendungssteuerung mithilfe von [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)erstellt wurde.

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

 

 




