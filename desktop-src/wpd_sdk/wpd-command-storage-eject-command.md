---
description: Der WPD \_ COMMAND \_ STORAGE \_ EJECT-Befehl wirft ein Speichermedium aus, das remote vom Computer ausgeworfen werden kann.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT Befehl (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839010"
---
# <a name="wpd_command_storage_eject-command"></a>\_WPD-BEFEHL \_ STORAGE \_ EJECT-Befehl

Der **WPD \_ COMMAND STORAGE \_ \_ EJECT-Befehl** wirft ein Speichermedium aus, das remote vom Computer ausjiziert werden kann.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ STORAGE**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                          | VarType    | Beschreibung                                             |
|------------------------------------|------------|---------------------------------------------------------|
| \_WPD-EIGENSCHAFT \_ – \_ SPEICHEROBJEKT-ID \_ | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des auswerfenden Speicherobjekts. |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                         | VarType   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**             | \_VT-FEHLER | Erforderlich. Ein **HRESULT,** das eine erfolgreiche oder nicht erfolgreiche Durchführung des Befehls angibt. Wenn der Aufrufer eine ungültige Anforderung vorgibt, sollte der Treiber **HRESULT \_ FROM \_ WIN32 (ERROR \_ NOT \_ SUPPORTED)** zurückgeben und muss keine anderen Ergebniswerte zurückgeben. Fehlercodes umfassen [Windows Fehlercodes für](error-constants.md) portable Geräte oder andere geeignete Fehlercodes. |
| **\_WPD-EIGENSCHAFT \_ COMMON DRIVER \_ ERROR \_ \_ CODE** | VT \_ UI4   | Optional. Ein treiberspezifischer Fehlercode. Dies wird in der Regel nur für Treibertests verwendet, oder wenn Treiber, Gerät und Client zusammen entworfen werden.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**IPortableDevice::SendCommand aufgerufen werden.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




