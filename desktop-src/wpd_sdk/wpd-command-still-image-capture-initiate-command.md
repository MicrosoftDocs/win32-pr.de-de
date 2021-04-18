---
description: Der Befehl zum \_ Initiieren der Image Erfassung durch den WPD-Befehl initiiert immer noch \_ \_ \_ \_ eine Image Erfassung durch ein Bild Funktions Objekt. Wenn ein neues Objekt erstellt wird, weil ein Bild erstellt wurde, sollte der Treiber das Ereignis Ereignis hinzufügen des WPD- \_ Ereignisses senden \_ \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE Befehl (portabledevice. h)
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
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364550"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Befehl zum \_ \_ Initiieren der \_ Image \_ Erfassung \_ für den WPD-Befehl

Der Befehl zum **Initiieren der \_ \_ \_ Image \_ Erfassung \_ durch den WPD-Befehl** initiiert immer noch eine Image Erfassung durch ein Bild Funktions Objekt. Wenn ein neues Objekt erstellt wird, weil ein Bild erstellt wurde, sollte der Treiber das Ereignis Ereignis **\_ \_ \_ Hinzufügen des WPD-Ereignisses** senden.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ trotzdem \_ Image \_ Erfassung**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                              | VarType    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeine WPD- \_ Eigenschaft ( \_ \_ Befehls \_ Ziel) | VT \_ LPWSTR | Erforderlich. Die Objekt-ID des noch Funktions Objekts der Bild Erfassung auf dem Gerät, das das Bild aufnehmen soll. Jedes funktionale Objekt für die Bild Erfassung kann über unterschiedliche Einstellungen verfügen, und es kann auf eine andere Hardware auf einem Gerät (z. b. eine Vorder-oder rückwärts Kamera eines Telefons) verweisen, und dieser Parameter gibt an, welcher Wert verwendet werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                         | VarType   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**             | VT- \_ Fehler | Erforderlich. Ein **HRESULT** , das den Erfolg oder Fehler beim Ausführen des Befehls angibt. Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben. Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes. |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code** | VT \_ UI4   | Dies ist optional. Ein Treiber spezifischer Fehlercode. Dieser Wert wird in der Regel von Geräte Anbietern verwendet, um die Diagnose von Gerätefehlern bei der Verwendung Ihrer Anwendungen zu verbessern. Anwendungen, die universell verwendet werden, würden Sie ignorieren und \_ \_ verwenden stattdessen ausschließlich das allgemeine HRESULT der WPD-Eigenschaft \_ .                                                                                                                   |



 

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

 

 




