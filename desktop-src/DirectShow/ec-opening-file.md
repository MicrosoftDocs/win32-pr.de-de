---
description: Das Diagramm öffnet eine Datei, oder das Öffnen einer Datei ist abgeschlossen.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361455"
---
# <a name="ec_opening_file"></a>EC- \_ öffnende \_ Datei

Das Diagramm öffnet eine Datei, oder das Öffnen einer Datei ist abgeschlossen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**True** , wenn das Diagramm beginnt, eine Datei zu öffnen, oder **false** , wenn das Diagramm die Datei nicht mehr öffnet.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Ein Filter kann dieses Ereignis senden, wenn es eine beträchtliche Zeit zum Öffnen einer Datei verbringt. (Die Datei befindet sich z. b. möglicherweise in einem Netzwerk.) Die Anwendung kann dieses Ereignis verwenden, um die Benutzeroberfläche anzupassen.

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

 

 




