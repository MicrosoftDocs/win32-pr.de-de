---
title: DRV_OPEN Meldung (Mmsystem.h)
description: Weist den Treiber an, eine neue Instanz zu öffnen.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 537d3067c85cf3f92eaf2fae81cd392490ff9fa728ed8377d8241c7204cf64e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691580"
---
# <a name="drv_open-message"></a>DRV \_ OPEN-Nachricht

Weist den Treiber an, eine neue Instanz zu öffnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Bezeichner des installierbaren Treibers.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiberinstanz.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Adresse einer auf NULL endenden Zeichenfolge mit Breitzeichen, die Konfigurationsinformationen angibt, die zum Öffnen der Instanz verwendet werden. Wenn keine Konfigurationsinformationen verfügbar sind, ist diese Zeichenfolge entweder leer, oder der Parameter ist **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32-Bit-Treiberspezifische Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich oder 0 (null) andernfalls .

## <a name="remarks"></a>Hinweise

Wenn der Treiber einen Wert ungleich 0 (null) zurückgibt, verwendet das System diesen Wert als Treiberbezeichner *(dwDriverId-Parameter)* in Nachrichten, die es anschließend an die Treiberinstanz sendet. Der Treiber kann einen beliebigen Werttyp als Bezeichner zurückgeben. Einige Treiber geben beispielsweise Speicheradressen zurück, die auf instanzspezifische Informationen verweisen. Wenn Sie diese Methode zum Angeben von Bezeichnern für eine Treiberinstanz verwenden, können die Treiber während der Verarbeitung von Nachrichten auf die Informationen zugreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treibermeldungen](installable-driver-messages.md)
</dt> </dl>

 

 





