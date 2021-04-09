---
title: Informationen zu roheingaben
description: In diesem Thema werden Benutzereingaben von Geräten, wie z. b. Joysticks, Touchscreens und Mikrofon, erläutert.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- Benutzereingabe, Rohdaten Eingabe
- Erfassen von Benutzereingaben, Rohdaten Eingabe
- Rohdaten Eingabe
- Registrieren unformatierender Eingaben
- Lesen von roheingaben
- Joystick-roheingabe
- unformatierte EINGABETASTE
- Mikrofon-roheingabe
- Eingabegerät (Human Interface Device, HID)
- HID (Eingabegeräte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3535e5601ec63a254c76060611999a1a2f08aeb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038983"
---
# <a name="about-raw-input"></a>Informationen zu roheingaben

Neben der herkömmlichen Tastatur und Maus gibt es viele Benutzereingabe-Geräte. Benutzereingaben können z. b. von einem Joystick, einem Touchscreen, einem Mikrofon oder anderen Geräten stammen, die eine hohe Flexibilität bei der Benutzereingabe ermöglichen. Diese Geräte werden kollektiv als Human Interface Devices (HIDS) bezeichnet. Die unformatierte Eingabe-API bietet eine stabile und robuste Möglichkeit für Anwendungen, unformatierte Eingaben von allen versteckten zu akzeptieren, einschließlich Tastatur und Maus.

Dieser Abschnitt enthält die folgenden Themen:

-   [Rohdaten Eingabe Modell](#raw-input-model)
-   [Registrierung für unformatierte Eingabe](#registration-for-raw-input)
-   [Lesen von roheingaben](#reading-raw-input)

## <a name="raw-input-model"></a>Rohdaten Eingabe Modell

Zuvor haben die Tastatur und die Maus normalerweise Eingabedaten generiert. Das System hat die Daten, die von diesen Geräten stammen, so interpretiert, dass die gerätespezifischen Details der Rohdaten entfernt wurden. Beispielsweise generiert die Tastatur den gerätespezifischen Überprüfungs Code, aber das System stellt eine Anwendung mit dem virtuellen Schlüsselcode bereit. Neben dem Ausblenden der Details der unformatierten Eingabe hat der Fenster-Manager nicht alle neuen HIDS unterstützt. Um Eingaben von den nicht unterstützten HIDS zu erhalten, musste eine Anwendung viele Aktionen ausführen: Öffnen Sie das Gerät, verwalten Sie den freigegebenen Modus, lesen Sie regelmäßig das Gerät, oder richten Sie den e/a-Abschlussport ein usw. Das Rohdaten Eingabe Modell und die zugehörigen APIs wurden entwickelt, um einfachen Zugriff auf unformatierte Eingaben von allen Eingabegeräten, einschließlich Tastatur und Maus, zuzulassen.

Das Rohdaten Eingabe Modell unterscheidet sich vom ursprünglichen Windows-Eingabe Modell für Tastatur und Maus. Im ursprünglichen Eingabe Modell empfängt eine Anwendung geräteunabhängige Eingaben in Form von Nachrichten, die an Ihre Fenster gesendet oder an diese gesendet werden, wie z. b. [**WM \_ char**](wm-char.md), [**WM \_ MouseMove**](wm-mousemove.md)und [**WM \_ appcommand**](wm-appcommand.md). Im Gegensatz dazu muss eine Anwendung für eine roheingabe die Geräte registrieren, von denen Sie Daten erhalten soll. Außerdem ruft die Anwendung die Rohdaten Eingabe über die [**WM- \_ Eingabe**](wm-input.md) Nachricht ab.

Es gibt mehrere Vorteile beim Rohdaten Eingabe Modell:

-   Das Eingabegerät muss von einer Anwendung nicht erkannt oder geöffnet werden.
-   Eine Anwendung ruft die Daten direkt vom Gerät ab und verarbeitet die Daten nach Ihren Anforderungen.
-   Eine Anwendung kann die Quelle der Eingabe unterscheiden, auch wenn Sie vom gleichen Gerätetyp ist. Beispielsweise zwei Maus Geräte.
-   Eine Anwendung verwaltet den Datenverkehr, indem Sie Daten aus einer Sammlung von Geräten oder nur bestimmten Gerätetypen angibt.
-   Versteckte Geräte können verwendet werden, wenn Sie im Marketplace verfügbar werden, ohne darauf zu warten, dass neue Nachrichten Typen oder ein aktualisiertes Betriebssystem neue Befehle in " [**WM \_ appcommand**](wm-appcommand.md)" aufweisen.

Beachten Sie, dass der [**WM \_ appcommand**](wm-appcommand.md) einige versteckte Geräte bereitstellt. " **WM \_ appcommand** " ist jedoch ein Geräte unabhängiges Eingabe Ereignis auf höherer Ebene, während mit der [**WM- \_ Eingabe**](wm-input.md) unformatierte Daten auf niedriger Ebene gesendet werden, die für ein Gerät spezifisch sind.

## <a name="registration-for-raw-input"></a>Registrierung für unformatierte Eingabe

Standardmäßig empfängt keine Anwendung unformatierte Eingaben. Um unformatierte Eingaben von einem Gerät zu erhalten, muss eine Anwendung das Gerät registrieren.

Zum Registrieren von Geräten erstellt eine Anwendung zunächst ein Array von [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) -Strukturen, die die [Sammlung der obersten Ebene](/windows-hardware/drivers/hid/top-level-collections) (TLC) für die gewünschten Geräte angeben. Der TLC wird von einer [Verwendungs Seite](/windows-hardware/drivers/hid/hid-usages#usage-page) (der-Klasse des Geräts) und einer [Nutzungs-ID](/windows-hardware/drivers/hid/hid-usages#usage-id) (dem Gerät innerhalb der-Klasse) definiert. Wenn Sie z. b. die Tastatur-TLC erhalten möchten, legen Sie UsagePage = 0x01 und startageid = 0x06 fest. Die Anwendung ruft [**registerrawinputdevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) auf, um die Geräte zu registrieren.

Beachten Sie, dass eine Anwendung ein Gerät registrieren kann, das zurzeit nicht mit dem System verbunden ist. Wenn dieses Gerät angefügt wird, sendet der Windows-Manager automatisch die unformatierte Eingabe an die Anwendung. Um die Liste der unformatierten Eingabegeräte auf dem System zu erhalten, ruft eine Anwendung " [**getrawinputdevicelist**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)" auf. Mithilfe des *hdevice* aus diesem Aufruf ruft eine Anwendung " [**getrawinputdeviceinfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) " auf, um die Geräteinformationen abzurufen.

Über den **dwFlags** -Member von [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)kann eine Anwendung die Geräte auswählen, auf die gelauscht werden soll, und auch die, die ignoriert werden sollen. Eine Anwendung kann z. b. Eingaben von allen Telefoniegeräten anfordern, außer bei der Beantwortung von Computern. Beispielcode finden Sie unter [registrieren für](using-raw-input.md)unformatierte Eingaben.

Beachten Sie, dass die Maus und die Tastatur auch HIDS sind, sodass Daten aus Ihnen sowohl die "HID Message [**WM \_**](wm-input.md) "-Eingabe als auch herkömmliche Nachrichten enthalten können. Eine Anwendung kann eine der beiden Methoden nach der richtigen Auswahl von Flags in [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)auswählen.

Wenn Sie den Registrierungsstatus einer Anwendung abrufen möchten, können Sie zu einem beliebigen Zeitpunkt [**getregisteredrawinputdevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) abrufen.

## <a name="reading-raw-input"></a>Lesen von roheingaben

Eine Anwendung empfängt unformatierte Eingaben von allen verstecken, deren Auflistung der [obersten Ebene](/windows-hardware/drivers/hid/top-level-collections) (TLC) mit einem TLC aus der Registrierung übereinstimmt. Wenn eine Anwendung unformatierte Eingaben empfängt, wird in der Nachrichten Warteschlange eine [**WM- \_ Eingabe**](wm-input.md) Nachricht angezeigt, und das Warteschlangen Status Flag **QS \_ rawinput** ist festgelegt (**QS- \_ Eingabe** enthält auch dieses Flag). Eine Anwendung kann Daten empfangen, wenn Sie sich im Vordergrund befindet, und wenn Sie sich im Hintergrund befindet.

Es gibt zwei Möglichkeiten, die Rohdaten zu lesen: die nicht gepufferte Methode (oder Standard) und die gepufferte Methode. Die nicht gepufferte Methode ruft die Rohdaten einer [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Struktur gleichzeitig ab und eignet sich für viele HIDS. Hier Ruft die Anwendung [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) auf, um die [**WM- \_ Eingabe**](wm-input.md) Nachricht zu erhalten. Anschließend ruft die Anwendung " [**getrawinputdata**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) " mit dem in " **WM \_ Input**" enthaltenen **rawinput** -Handle auf. Ein Beispiel finden Sie unter [Durchführung eines Standard-Lese](using-raw-input.md)Vorgang für unformatierte Eingaben.

Im Gegensatz dazu wird von der gepufferten Methode jeweils ein Array von [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Strukturen abgerufen. Dies wird für Geräte bereitgestellt, die große Mengen an unformatierten Eingaben verursachen können. In dieser Methode ruft die Anwendung " [**getrawinputbuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) " auf, um ein Array von **rawinput** -Strukturen zu erhalten. Beachten Sie, dass das [**nextrawinputblock**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) -Makro verwendet wird, um ein Array von **rawinput** -Strukturen zu durchlaufen. Ein Beispiel finden Sie unter [Durchführung eines gepufferten gelesenen gelesenen Daten](using-raw-input.md).

Um die unformatierte Eingabe zu interpretieren, sind ausführliche Informationen zu den HIDS erforderlich. Eine Anwendung ruft die Geräteinformationen ab, indem Sie " [**getrawinputdeviceinfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) " mit dem Geräte handle aufrufen. Dieses Handle kann entweder von [**WM- \_ Eingaben**](wm-input.md) oder vom **hdevice** -Member von [**rawinpuderader**](/windows/win32/api/winuser/ns-winuser-rawinputheader)stammen.