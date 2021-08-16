---
title: Informationen zu Rohdateneingaben
description: In diesem Thema werden Benutzereingaben von Geräten wie z. B. Sprechflächen, Touchscreens und Mikrofone erläutert.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- Benutzereingabe, Rohdateneingabe
- Erfassen von Benutzereingaben, Rohdateneingaben
- Rohdateneingabe
- Registrieren von Rohdateneingaben
- Lesen von unformatierten Eingaben
- raw input
- Unformatierte Eingabe auf dem Touchbildschirm
- Unformatierte Mikrofoneingabe
- Eingabegerät (Human Interface Device, HID)
- HID (Eingabegeräte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fed3772406cc85df57b95c4b11dbcfeaf60804e94da5602059ec790e87e0439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884327"
---
# <a name="about-raw-input"></a>Informationen zu Rohdateneingaben

Neben der herkömmlichen Tastatur und Maus gibt es viele Benutzereingabegeräte. Benutzereingaben können z. B. aus einem Kabel, einem Touchscreen, einem Mikrofon oder anderen Geräten stammen, die eine große Flexibilität bei der Benutzereingabe ermöglichen. Diese Geräte werden zusammen als Human Interface Devices (HIDs) bezeichnet. Die RAW-Eingabe-API bietet eine stabile und stabile Möglichkeit für Anwendungen, unformatierte Eingaben von beliebigen HID-Dateien zu akzeptieren, einschließlich Tastatur und Maus.

Dieser Abschnitt enthält die folgenden Themen:

-   [Rohdaten-Eingabemodell](#raw-input-model)
-   [Registrierung für Rohdateneingaben](#registration-for-raw-input)
-   [Lesen von Unformatierten Eingaben](#reading-raw-input)

## <a name="raw-input-model"></a>Rohdaten-Eingabemodell

Zuvor haben Tastatur und Maus in der Regel Eingabedaten generiert. Das System interpretierte die von diesen Geräten stammenden Daten so, dass die gerätespezifischen Details der Rohdaten entfernt wurden. Beispielsweise generiert die Tastatur den gerätespezifischen Scancode, aber das System stellt eine Anwendung mit dem virtuellen Schlüsselcode bereit. Neben dem Ausblenden der Details der unformatierten Eingabe unterstützte der Fenster-Manager nicht alle neuen HIDs. Um Eingaben von den nicht unterstützten HIDs zu erhalten, musste eine Anwendung viele Dinge tun: Öffnen des Geräts, Verwalten des freigegebenen Modus, regelmäßiges Lesen des Geräts oder Einrichten des E/A-Abschlussports usw. Das Rohdateneingabemodell und die zugehörigen APIs wurden entwickelt, um einfachen Zugriff auf unformatierte Eingaben von allen Eingabegeräten, einschließlich Tastatur und Maus, zu ermöglichen.

Das rohe Eingabemodell unterscheidet sich vom ursprünglichen Windows Eingabemodell für Tastatur und Maus. Im ursprünglichen Eingabemodell empfängt eine Anwendung geräteunabhängige Eingaben in Form von Nachrichten, die an ihre Fenster gesendet oder gesendet werden, z. B. [**WM \_ CHAR,**](wm-char.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)und [**WM \_ APPCOMMAND**](wm-appcommand.md). Im Gegensatz dazu muss eine Anwendung für rohe Eingaben die Geräte registrieren, von der sie Daten abrufen möchte. Außerdem ruft die Anwendung die Rohdateneingabe über die [**WM \_ INPUT-Nachricht**](wm-input.md) ab.

Das Rohdateneingabemodell bietet mehrere Vorteile:

-   Eine Anwendung muss das Eingabegerät nicht erkennen oder öffnen.
-   Eine Anwendung ruft die Daten direkt vom Gerät ab und verarbeitet die Daten für ihre Anforderungen.
-   Eine Anwendung kann die Quelle der Eingabe auch dann unterscheiden, wenn sie vom gleichen Gerätetyp ist. Beispielsweise zwei Mausgeräte.
-   Eine Anwendung verwaltet den Datenverkehr, indem Daten aus einer Sammlung von Geräten oder nur bestimmten Gerätetypen angegeben werden.
-   HID-Geräte können verwendet werden, sobald sie im Marketplace verfügbar werden, ohne auf neue Nachrichtentypen oder ein aktualisiertes Betriebssystem zu warten, um neue Befehle in [**WM \_ APPCOMMAND**](wm-appcommand.md)zu erhalten.

Beachten Sie, dass [**WM \_ APPCOMMAND**](wm-appcommand.md) einige HID-Geräte bereitstellt. WM **\_ APPCOMMAND** ist jedoch ein geräteunabhängiges Eingabeereignis auf höherer Ebene, während [**WM \_ INPUT**](wm-input.md) unformatierte Daten auf niedriger Ebene sendet, die für ein Gerät spezifisch sind.

## <a name="registration-for-raw-input"></a>Registrierung für Rohdateneingaben

Standardmäßig empfängt keine Anwendung rohe Eingaben. Um rohe Eingaben von einem Gerät zu empfangen, muss eine Anwendung das Gerät registrieren.

Um Geräte zu registrieren, erstellt eine Anwendung zunächst ein Array von [**RAWINPUTDEVICE-Strukturen,**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) die die Sammlung der obersten Ebene (Top [Level Collection,](/windows-hardware/drivers/hid/top-level-collections) TLC) für die gewünschten Geräte angeben. Der TLC wird durch eine [Nutzungsseite](/windows-hardware/drivers/hid/hid-usages#usage-page) (die Klasse des Geräts) und eine [Nutzungs-ID](/windows-hardware/drivers/hid/hid-usages#usage-id) (das Gerät innerhalb der Klasse) definiert. Um beispielsweise den Tastatur-TLC abzurufen, legen Sie UsagePage = 0x01 und UsageID = 0x06 fest. Die Anwendung ruft [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) auf, um die Geräte zu registrieren.

Beachten Sie, dass eine Anwendung ein Gerät registrieren kann, das derzeit nicht an das System angeschlossen ist. Wenn dieses Gerät angeschlossen ist, sendet der Windows Manager die Rohdateneingabe automatisch an die Anwendung. Um die Liste der unformatierten Eingabegeräte auf dem System abzurufen, ruft eine Anwendung [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)auf. Mithilfe des *hDevice* aus diesem Aufruf ruft eine Anwendung [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) auf, um die Geräteinformationen abzurufen.

Über das **dwFlags-Mitglied** von [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)kann eine Anwendung die Geräte auswählen, auf die gelacht werden soll, sowie die Geräte, die ignoriert werden sollen. Eine Anwendung kann z. B. Eingaben von allen Telefoniegeräten mit Ausnahme von Antwortcomputern anfordern. Beispielcode finden Sie unter [Registrieren für rohe Eingabe.](using-raw-input.md)

Beachten Sie, dass Maus und Tastatur ebenfalls HIDs sind, sodass Daten von ihnen sowohl über die [**\_ WM-EINGABE**](wm-input.md) der HID-Nachricht als auch aus herkömmlichen Nachrichten stammen können. Eine Anwendung kann eine der beiden Methoden auswählen, indem sie in [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)die richtigen Flags auswählt.

Rufen Sie jederzeit [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) auf, um den Registrierungsstatus einer Anwendung abzurufen.

## <a name="reading-raw-input"></a>Lesen von Unformatierten Eingaben

Eine Anwendung empfängt unformatierte Eingaben von jedem HID, dessen Sammlung auf oberster Ebene (Top [Level Collection,](/windows-hardware/drivers/hid/top-level-collections) TLC) mit einem TLC aus der Registrierung übereinstimmt. Wenn eine Anwendung unformatierte Eingaben empfängt, erhält ihre Nachrichtenwarteschlange eine [**WM \_ INPUT-Nachricht,**](wm-input.md) und das Warteschlangenstatusflag **QS \_ RAWINPUT** ist festgelegt **(QS \_ INPUT** enthält auch dieses Flag). Eine Anwendung kann Daten empfangen, wenn sie sich im Vordergrund und im Hintergrund befindet.

Es gibt zwei Möglichkeiten, die Rohdaten zu lesen: die nicht gepufferte Methode (oder die Standardmethode) und die gepufferte Methode. Die nicht gepufferte Methode ruft die Rohdaten jeweils eine [**RAWINPUT-Struktur**](/windows/win32/api/winuser/ns-winuser-rawinput) ab und ist für viele HIDs geeignet. Hier ruft die Anwendung [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) auf, um die [**\_ WM-EINGABEnachricht**](wm-input.md) abzurufen. Anschließend ruft die Anwendung [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) mithilfe des **RAWINPUT-Handles** auf, das in WM INPUT enthalten **ist. \_** Ein Beispiel finden Sie unter [Doing a Standard Read of Raw Input](using-raw-input.md).

Im Gegensatz dazu ruft die gepufferte Methode gleichzeitig ein Array von [**RAWINPUT-Strukturen**](/windows/win32/api/winuser/ns-winuser-rawinput) ab. Dies wird für Geräte bereitgestellt, die große Mengen von Rohdateneingaben erzeugen können. In dieser Methode ruft die Anwendung [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) auf, um ein Array von **RAWINPUT-Strukturen** abzurufen. Beachten Sie, dass das [**NEXTRAWINPUTBLOCK-Makro**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) verwendet wird, um ein Array von **RAWINPUT-Strukturen** zu durchlaufen. Ein Beispiel finden Sie unter [Doing a Buffered Read of Raw Input](using-raw-input.md).

Um die Rohdateneingabe zu interpretieren, sind ausführliche Informationen zu den HIDs erforderlich. Eine Anwendung ruft die Geräteinformationen ab, indem [**getRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) mit dem Gerätehandle aufgerufen wird. Dieses Handle kann entweder von [**WM \_ INPUT**](wm-input.md) oder vom **hDevice-Member** von [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)stammen.