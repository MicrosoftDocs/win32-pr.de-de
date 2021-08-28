---
description: Der Befehl WPD \_ COMMAND STORAGE FORMAT format \_ \_ formatiert ein speicherfunktionales Objekt auf dem Gerät.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT-Befehl (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 353710bc4167b626b6af001ef535f6d21538a328609aaf05e5e8846415485914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806200"
---
# <a name="wpd_command_storage_format-command"></a>BEFEHL \_ \_ "WPD COMMAND STORAGE \_ FORMAT"

Der Befehl **WPD \_ COMMAND STORAGE \_ \_ FORMAT** format formatiert ein speicherfunktionales Objekt auf dem Gerät.

## <a name="command-category"></a>Befehlskategorie

**\_ \_ WPD-KATEGORIESPEICHER**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                          | VarType    | Beschreibung                                              |
|------------------------------------|------------|----------------------------------------------------------|
| SPEICHEROBJEKT-ID DER \_ \_ \_ \_ WPD-EIGENSCHAFT | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des zu formatierende Speichermediums. |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




