---
description: Mit dem Befehl WPD COMMAND COMMON RESET DEVICE wird \_ \_ das Gerät \_ \_ zurückgesetzt. Dies bedeutet nicht, dass neu formatiert wird. dies entspricht dem Ein- und Ausschalten des Geräts.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE-Befehl (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b6a492b7017b8ace6c9118c2f08a1761d7785277fb497474d3e9f39aad60ae8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083373"
---
# <a name="wpd_command_common_reset_device-command"></a>\_WPD-BEFEHL \_ COMMON RESET \_ DEVICE \_ Command

Mit dem Befehl **WPD \_ COMMAND COMMON RESET \_ \_ \_ DEVICE** wird das Gerät zurückgesetzt. Dies bedeutet nicht, dass neu formatiert wird. dies entspricht dem Ein- und Ausschalten des Geräts.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ COMMON**

## <a name="parameters"></a>Parameter

Dieser Befehl weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                         | VarType   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**             | \_VT-FEHLER | Erforderlich. Ein **HRESULT,** das angibt, ob der Befehl erfolgreich ausgeführt wurde oder nicht ausgeführt werden kann. Wenn der Aufrufer eine ungültige Anforderung stellt, sollte der Treiber **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** zurückgeben und muss keine anderen Ergebniswerte zurückgeben. Fehlercodes umfassen [Windows Fehlercodes für portable Geräte](error-constants.md) oder andere geeignete Fehlercodes. |
| **ALLGEMEINER \_ \_ \_ \_ TREIBERFEHLERCODE \_ FÜR WPD-EIGENSCHAFTEN** | VT \_ UI4   | Optional. Ein treiberspezifischer Fehlercode. Dies wird in der Regel nur für Treibertests verwendet, oder wenn Treiber, Gerät und Client alle zusammen entworfen wurden.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




