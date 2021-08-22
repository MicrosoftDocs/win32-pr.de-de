---
description: Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499f05a26f3fa1387347929f5c14a64b1f440a53ed9b5fd17830d582fb640c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015938"
---
# <a name="ec_loadstatus"></a>EC \_ LOADSTATUS

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

## <a name="remarks"></a>Hinweise

Der [WM ASF-Readerfilter](wm-asf-reader-filter.md) und der Legacyfilter [Windows Medienquelle](windows-media-source-filter.md) senden dieses Ereignis. Der erste Ereignisparameter weist einen der folgenden Werte auf.



| Wert                        | Beschreibung                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ CLOSED       | Der Quellfilter hat die Datei geschlossen.         |
| AM \_ LOADSTATUS \_ CONNECTING   | Der Quellfilter stellt eine Verbindung mit dem Server her. |
| AM \_ LOADSTATUS \_ LOADINGDESCR | Wird nicht verwendet.                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | Nicht verwendet                                       |
| AM \_ LOADSTATUS \_ LOCATING     | Der Quellfilter sucht nach angeforderten Daten.  |
| AM \_ LOADSTATUS \_ OPEN         | Der Quellfilter hat die Datei geöffnet.         |
| AM \_ LOADSTATUS \_ OPENING      | Der Quellfilter öffnet die Datei.         |



 

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

 

 




