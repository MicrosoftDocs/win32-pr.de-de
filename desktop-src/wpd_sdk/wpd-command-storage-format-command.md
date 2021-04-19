---
description: Der Befehl " \_ Befehl \_ Speicher \_ Format" in WPD formatiert ein Speicher funktionales Objekt auf dem Gerät.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT Befehl (portabledevice. h)
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
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370231"
---
# <a name="wpd_command_storage_format-command"></a>Befehl " \_ \_ Speicher \_ Format für WPD-Befehl"

Der Befehl " **\_ Befehl \_ Speicher \_ Format" in WPD** formatiert ein Speicher funktionales Objekt auf dem Gerät.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ - \_ kategoriespeicher**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                          | VarType    | BESCHREIBUNG                                              |
|------------------------------------|------------|----------------------------------------------------------|
| WPD- \_ Eigenschaften \_ Speicher Objekt- \_ \_ ID | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des zu formatierenden Speichermediums. |



 

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

 

 




