---
description: Mit dem Befehl "WPD \_ Command \_ Storage \_ eject" wird ein Speichermedium eingefügt, das per Remote Zugriff vom Computer entfernt werden kann.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT Befehl (portabledevice. h)
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
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361604"
---
# <a name="wpd_command_storage_eject-command"></a>Befehl "Speicher für WPD- \_ Befehl" \_ \_

Mit dem Befehl " **WPD \_ Command \_ Storage \_ eject** " wird ein Speichermedium eingefügt, das per Remote Zugriff vom Computer entfernt werden kann.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ - \_ kategoriespeicher**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                          | VarType    | BESCHREIBUNG                                             |
|------------------------------------|------------|---------------------------------------------------------|
| WPD- \_ Eigenschaften \_ Speicher Objekt- \_ \_ ID | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des zu ausgelösten Speicher Objekts. |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                         | VarType   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**             | VT- \_ Fehler | Erforderlich. Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt. Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben. Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes. |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code** | VT \_ UI4   | Dies ist optional. Ein Treiber spezifischer Fehlercode. Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




