---
description: Der \_ WPD COMMAND \_ STILL IMAGE \_ CAPTURE \_ \_ INITIATE-Befehl initiiert eine Standbilderfassung durch ein funktionstüchtiger Objekt des Stillbilds. Wenn ein neues -Objekt als Ergebnis der Aufnahme eines Bilds erstellt wird, sollte der Treiber das WPD \_ EVENT \_ OBJECT \_ ADDED-Ereignis senden.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE-Befehl (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5c5490a5af583753f504decacaccf4b4373890fdb7f0e5b099389df29cdc0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806280"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>\_WPD-BEFEHL \_ STILL IMAGE \_ CAPTURE \_ \_ INITIATE-Befehl

Der **WPD \_ COMMAND STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE-Befehl** initiiert eine Standbilderfassung durch ein funktionstüchtiger Objekt des Stillbilds. Wenn ein neues -Objekt als Ergebnis der Aufnahme eines Bilds erstellt wird, sollte der Treiber das **WPD \_ EVENT OBJECT \_ \_ ADDED-Ereignis** senden.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                              | VarType    | Beschreibung                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ ALLGEMEINES \_ \_ BEFEHLSZIEL DER WPD-EIGENSCHAFT | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des Funktionsobjekts für die Aufzeichnung des Stillbilds auf dem Gerät, das das Bild aufnehmen soll. Jedes Funktionsobjekt für die Bildaufnahme kann unterschiedliche Einstellungen aufweisen und kann auf verschiedene Hardware auf einem Gerät verweisen (z. B. eine Vorder- oder Rückkamera eines Telefons), und dieser Parameter gibt an, welche Verwendet werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                         | VarType   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**             | \_VT-FEHLER | Erforderlich. Ein **HRESULT,** das angibt, ob der Befehl erfolgreich ausgeführt wurde oder nicht ausgeführt werden kann. Wenn der Aufrufer eine ungültige Anforderung stellt, sollte der Treiber **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** zurückgeben und muss keine anderen Ergebniswerte zurückgeben. Fehlercodes umfassen [Windows Fehlercodes für portable Geräte](error-constants.md) oder andere geeignete Fehlercodes. |
| **ALLGEMEINER \_ \_ \_ \_ TREIBERFEHLERCODE \_ FÜR WPD-EIGENSCHAFTEN** | VT \_ UI4   | Optional. Ein treiberspezifischer Fehlercode. Dieser Wert wird in der Regel von Geräteanbietern verwendet, um die Diagnose von Gerätefehlern bei der Verwendung ihrer Anwendungen zu verbessern. Allgemeine Anwendungen würden dies ignorieren und sich stattdessen ausschließlich auf WPD \_ PROPERTY \_ COMMON \_ HRESULT verlassen.                                                                                                                   |



 

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

 

 




