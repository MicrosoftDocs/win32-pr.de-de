---
description: Das Diagramm öffnet eine Datei oder hat das Öffnen einer Datei beendet.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 436a48a90640577504871dfe835d6c81c398680ae070065189cb4031493e7fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079120"
---
# <a name="ec_opening_file"></a>EC \_ OPENING \_ FILE

Das Diagramm öffnet eine Datei oder hat das Öffnen einer Datei beendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**TRUE,** wenn das Diagramm beginnt, eine Datei zu öffnen, oder **FALSE,** wenn das Diagramm die Datei nicht mehr öffnet.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Ein Filter kann dieses Ereignis senden, wenn er viel Zeit mit dem Öffnen einer Datei verbringt. (Die Datei kann sich beispielsweise in einem Netzwerk befinden.) Die Anwendung kann dieses Ereignis verwenden, um die Benutzeroberfläche anzupassen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




