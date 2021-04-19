---
description: Der SMS-Send-Befehl des WPD- \_ Befehls \_ \_ initiiert das Senden einer SMS-Nachricht (Short Message Service) durch ein SMS-Funktions Objekt.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: WPD_COMMAND_SMS_SEND Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369449"
---
# <a name="wpd_command_sms_send-command"></a>Befehl " \_ \_ SMS \_ Senden" in WPD-Befehl

Der **SMS- \_ \_ \_ Send** -Befehl des WPD-Befehls initiiert das Senden einer SMS-Nachricht (Short Message Service) durch ein SMS-Funktions Objekt.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ SMS**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                              | VarType             | BESCHREIBUNG                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel) | VT \_ LPWSTR          | Erforderlich. Die Objekt-ID des SMS-Funktions Objekts, das die Nachricht senden soll. Verschiedene SMS-funktionale Objekte können unterschiedliche Einstellungen aufweisen.                                                                                     |
| SMS-Empfänger der WPD- \_ Eigenschaft \_ \_          | VT \_ LPWSTR          | Erforderlich. Der URI des Empfängers.                                                                                                                                                                                                  |
| SMS- \_ \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft      | VT \_ UI4             | Erforderlich. Ein [**SMS- \_ Nachrichten \_ Typen**](sms-message-types.md) Enumerator, der den Typ der Nachricht angibt (Text oder binär).                                                                                                        |
| SMS- \_ \_ \_ Text \_ Nachricht für WPD-Eigenschaft      | VT \_ LPWSTR          | Dies ist optional. Wenn der **\_ SMS- \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft** eine Textnachricht angibt, ist dies die Meldungs Zeichenfolge; andernfalls wird dieser Parameter nicht eingeschlossen.                                                                                  |
| WPD- \_ Eigenschaft, \_ SMS- \_ Binär \_ Nachricht    | VT \_ Vector \| VT \_ UI1 | Dies ist optional. Wenn der **\_ SMS- \_ \_ \_ Nachrichtentyp der WPD-Eigenschaft** eine binäre Nachricht angibt, ist dies ein Zeiger auf ein Bytearray. andernfalls ist dieser Parameter nicht eingeschlossen. Das erste DWORD des Werts ist die Länge des Arrays in Bytes. |



 

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

 

 




