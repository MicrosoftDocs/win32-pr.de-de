---
description: Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358738"
---
# <a name="ec_loadstatus"></a>EC- \_ loadstatus

Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Statuscode. Siehe Hinweise.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter und der ältere [Windows Media-Quell](windows-media-source-filter.md) Filter Senden dieses Ereignis. Der erste Ereignis Parameter hat einen der folgenden Werte.



| Wert                        | BESCHREIBUNG                                    |
|------------------------------|------------------------------------------------|
| AM \_ loadstatus \_ geschlossen       | Der Quell Filter hat die Datei geschlossen.         |
| AM \_ loadstatus- \_ Verbindung   | Der Quell Filter stellt eine Verbindung mit dem Server her. |
| AM \_ loadstatus \_ loadingdescr | Nicht verwendet.                                      |
| AM \_ loadstatus \_ loadingmcast | Nicht verwendet                                       |
| AM \_ loadstatus \_ Suchen     | Der Quell Filter sucht die angeforderten Daten.  |
| AM \_ loadstatus \_ geöffnet         | Der Quell Filter hat die Datei geöffnet.         |
| AM \_ loadstatus \_ Öffnen      | Der Quell Filter öffnet die Datei.         |



 

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

 

 




