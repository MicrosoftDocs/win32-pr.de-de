---
title: Rohdateneingabe
description: In diesem Abschnitt wird beschrieben, wie das System rohe Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows Benutzeroberfläche, Benutzereingabe
- Windows Benutzeroberfläche, Rohdateneingabe
- Benutzereingabe, Rohdateneingabe
- Erfassen von Benutzereingaben, Rohdateneingaben
- Rohdateneingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e26d67f2b014ce22c2d01cb4738cca4e041c59e417a216f0d75ffef6e6e4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482756"
---
# <a name="raw-input"></a>Rohdateneingabe

In diesem Abschnitt wird beschrieben, wie das System rohe Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet. Rohdateneingaben werden manchmal als generische Eingaben bezeichnet.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                           | Beschreibung                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Informationen zu Rohdateneingaben](about-raw-input.md)         | Erläutert Benutzereingaben von Geräten wie z. B. Geräte, Touchscreens und Mikrofone.<br/> |
| [Verwenden von Rohdateneingaben](using-raw-input.md)         | Stellt Beispielcode für Aufgaben im Zusammenhang mit unformatierten Eingaben bereit.<br/>                                |
| [Rohdateneingabereferenz](raw-input-reference.md) | Enthält den API-Verweis.<br/>                                                          |



 

### <a name="functions"></a>Functions



| Name                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Ruft die standardmäßige unformatierte Eingabeprozedur auf, um die Standardverarbeitung für alle unformatierten Eingabenachrichten bereitzustellen, die von einer Anwendung nicht verarbeitet werden. Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird. [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) wird mit den gleichen Parametern aufgerufen, die von der Fensterprozedur empfangen werden. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Führt einen gepufferten Leselauf der Rohdaten aus.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Ruft die unformatierte Eingabe vom angegebenen Gerät ab.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Ruft Informationen zum unformatierten Eingabegerät ab.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Listet die unformatierten Eingabegeräte auf, die an das System angefügt sind. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Ruft die Informationen zu den unformatierten Eingabegeräten für die aktuelle Anwendung ab.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registriert die Geräte, die die rohen Eingabedaten bereitstellen.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Makros



| Name                                                            | Beschreibung                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Ruft den Eingabecode aus *wParam* in [**WM \_ INPUT**](wm-input.md)ab.<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Ruft die Position der nächsten -Struktur in einem Array von [**RAWINPUT-Strukturen**](/windows/win32/api/winuser/ns-winuser-rawinput) ab. <br/> |



 

### <a name="notifications"></a>Benachrichtigungen



| Name                                                        | Beschreibung                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_WM-EINGABE**](wm-input.md)                               | Wird an das Fenster gesendet, das rohe Eingaben erhält. <br/>            |
| [**WM \_ INPUT \_ DEVICE \_ CHANGE**](wm-input-device-change.md) | Wird an das Fenster gesendet, das für den Empfang unformatierten Eingaben registriert wurde. <br/> |



 

### <a name="structures"></a>Strukturen



| Name                                                            | Beschreibung                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Beschreibt das Format der unformatierten Eingabe aus einem Eingabegeräte (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Enthält die unformatierte Eingabe eines Geräts. <br/>                                      |
| [**Rawinputdevice**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Definiert Informationen für die unformatierten Eingabegeräte. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Enthält Informationen zu einem unformatierten Eingabegerät.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Enthält die Headerinformationen, die Teil der rohen Eingabedaten sind. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Enthält Informationen zum Zustand der Tastatur. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Enthält Informationen zum Zustand der Maus. <br/>                         |
| [**RID \_ DEVICE \_ INFO**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Definiert die rohen Eingabedaten, die von einem beliebigen Gerät stammen. <br/>                         |
| [**RID \_ DEVICE \_ INFO \_ HID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Definiert die rohen Eingabedaten, die aus dem angegebenen HID stammen. <br/>                  |
| [**RID \_ DEVICE \_ INFO \_ KEYBOARD**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Definiert die unformatierten Eingabedaten, die von der angegebenen Tastatur stammen. <br/>             |
| [**RID \_ DEVICE \_ INFO \_ MOUSE**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Definiert die unformatierten Eingabedaten, die von der angegebenen Maus stammen.<br/>                 |



 

 

