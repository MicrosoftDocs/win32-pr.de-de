---
title: DRV_CLOSE Nachricht (Mmsystem.h)
description: Weist den Treiber an, die angegebene Instanz zu schließen. Wenn keine anderen Instanzen geöffnet sind, sollte sich der Treiber auf die nachfolgende Freigabe aus dem Arbeitsspeicher vorbereiten.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d89be1821b03e43fbe05b5ed2efc90e40db03e36538cf0412201baa7273e596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622667"
---
# <a name="drv_close-message"></a>DRV \_ CLOSE-Meldung

Weist den Treiber an, die angegebene Instanz zu schließen. Wenn keine anderen Instanzen geöffnet sind, sollte sich der Treiber auf die nachfolgende Freigabe aus dem Arbeitsspeicher vorbereiten.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Bezeichner des installierbaren Treibers. Dies ist derselbe Wert, der zuvor vom Treiber aus der [**DRV \_ OPEN-Nachricht**](drv-open.md) zurückgegeben wurde.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiberinstanz.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

32-Bit-Wert, der als *lParam1-Parameter* in einem Aufruf der **DriverClose-Funktion** angegeben wird.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32-Bit-Wert, der als *lParam2-Parameter* in einem Aufruf der **DriverClose-Funktion** angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treibermeldungen](installable-driver-messages.md)
</dt> </dl>

 

 





