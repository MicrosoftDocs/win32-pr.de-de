---
title: Rohdaten Eingabe
description: In diesem Abschnitt wird beschrieben, wie das System unformatierte Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, Rohdaten Eingabe
- Benutzereingabe, Rohdaten Eingabe
- Erfassen von Benutzereingaben, Rohdaten Eingabe
- Rohdaten Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390245"
---
# <a name="raw-input"></a>Rohdaten Eingabe

In diesem Abschnitt wird beschrieben, wie das System unformatierte Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet. Unformatierte Eingaben werden manchmal auch als generische Eingaben bezeichnet.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                           | BESCHREIBUNG                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Informationen zu roheingaben](about-raw-input.md)         | Erläutert Benutzereingaben von Geräten wie z. b. Joysticks, Touchscreens und Mikrofonen.<br/> |
| [Verwenden von Rohdateneingaben](using-raw-input.md)         | Stellt Beispielcode für Aufgaben im Zusammenhang mit unformatierten Eingaben bereit.<br/>                                |
| [Unformatierte Eingabe Referenz](raw-input-reference.md) | Enthält die API-Referenz.<br/>                                                          |



 

### <a name="functions"></a>Functions



| Name                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Entfrawinputproc"**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Ruft die standardmäßige unformatierte Eingabe Prozedur auf, um die Standard Verarbeitung für alle unformatierten Eingabe Nachrichten bereitzustellen, die eine Anwendung nicht verarbeitet Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird. [**Defrawinputproc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) wird mit denselben Parametern aufgerufen, die von der Fenster Prozedur empfangen werden. <br/> |
| [**Getrawinputbuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Führt einen gepufferten Lesevorgang für die Rohdaten der Eingabe aus.<br/>                                                                                                                                                                                                                                                              |
| [**Getrawinputdata**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Ruft die unformatierte Eingabe vom angegebenen Gerät ab.<br/>                                                                                                                                                                                                                                                                |
| [**Getrawinputdeaktiviert**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Ruft Informationen über das roheingabe Gerät ab.<br/>                                                                                                                                                                                                                                                                 |
| [**Getrawinputdevicelist**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Listet die unformatierten Eingabegeräte auf, die mit dem System verbunden sind. <br/>                                                                                                                                                                                                                                                    |
| [**Getregisteredrawinputdevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Ruft die Informationen zu den unformatierten Eingabegeräten für die aktuelle Anwendung ab.<br/>                                                                                                                                                                                                                                |
| [**Registerrawinputdevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registriert die Geräte, die die Rohdaten für die Eingabe bereitstellen.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Makros



| Name                                                            | BESCHREIBUNG                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**GET \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Ruft den Eingabecode von *wParam* in der [**WM- \_ Eingabe**](wm-input.md)ab.<br/>                              |
| [**Nextrawinputblock**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Ruft den Speicherort der nächsten-Struktur in einem Array von [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Strukturen ab. <br/> |



 

### <a name="notifications"></a>Benachrichtigungen



| Name                                                        | BESCHREIBUNG                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**WM- \_ Eingabe**](wm-input.md)                               | Wird an das Fenster gesendet, das roheingaben erhält. <br/>            |
| [**WM- \_ Eingabe \_ Geräte \_ Änderung**](wm-input-device-change.md) | Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist. <br/> |



 

### <a name="structures"></a>Strukturen



| Name                                                            | BESCHREIBUNG                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Rawhid**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Beschreibt das Format der unformatierten Eingabe von einem Eingabegeräte (HID). <br/> |
| [**Rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Enthält die unformatierte Eingabe von einem Gerät. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Definiert Informationen für die unformatierten Eingabegeräte. <br/>                             |
| [**Rawinputdevicelist**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Enthält Informationen zu einem unformatierten Eingabegerät.<br/>                              |
| [**Rawinpuderader**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Enthält die Header Informationen, die Teil der Rohdaten für die Eingabe sind. <br/>        |
| [**Rawkeyboard**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Enthält Informationen zum Zustand der Tastatur. <br/>                      |
| [**Rawmouse**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Enthält Informationen über den Zustand der Maus. <br/>                         |
| [**Info zum RID- \_ Gerät \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Definiert die unformatierten Eingabedaten, die von einem beliebigen Gerät stammen. <br/>                         |
| [**Rid- \_ Geräte \_ Informationen \_ verborgen**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Definiert die unformatierten Eingabedaten, die aus dem angegebenen HID stammen. <br/>                  |
| [**\_ \_ Info \_ Tastatur für Rid-Gerät**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Definiert die unformatierten Eingabedaten, die von der angegebenen Tastatur stammen. <br/>             |
| [**Info-Maus des RID- \_ Geräts \_ \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Definiert die unformatierten Eingabedaten, die von der angegebenen Maus stammen.<br/>                 |



 

 

