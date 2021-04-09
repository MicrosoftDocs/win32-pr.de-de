---
title: DRV_OPEN Meldung (MMSYSTEM. h)
description: Weist den Treiber an, eine neue-Instanz zu öffnen.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN-Nachricht (Multimedia)
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
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106221"
---
# <a name="drv_open-message"></a>DRV- \_ Open-Nachricht

Weist den Treiber an, eine neue-Instanz zu öffnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*
</dt> <dd>

Der Bezeichner des installierbaren Treibers.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiber Instanz.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Adresse einer null-terminierten Zeichenfolge mit breit Zeichen, die Konfigurationsinformationen angibt, die zum Öffnen der-Instanz verwendet werden. Wenn keine Konfigurationsinformationen verfügbar sind, ist entweder diese Zeichenfolge leer, oder der-Parameter ist **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32-Bit-Treiber spezifische Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Wenn der Treiber einen Wert ungleich 0 (null) zurückgibt, verwendet das System diesen Wert als Treiber Bezeichner (den *dwdriverid* -Parameter) in Nachrichten, die er anschließend an die Treiber Instanz sendet. Der Treiber kann jeden Werttyp als Bezeichner zurückgeben. Einige Treiber geben z. b. Speicheradressen zurück, die auf instanzspezifische Informationen verweisen. Die Verwendung dieser Methode zum Angeben von bezeichern für eine Treiber Instanz ermöglicht den Treibern den Zugriff auf die Informationen, während diese Nachrichten verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treiber Meldungen](installable-driver-messages.md)
</dt> </dl>

 

 





