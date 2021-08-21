---
title: XInput-Versionen
description: XInput ist eine plattformübergreifende API, die zur Verwendung auf Xbox und Windows ausgeliefert wurde.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277712308ca6083147d10138ba4d78e7e0fa086df95a78ab2b8317abca567dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430783"
---
# <a name="xinput-versions"></a>XInput-Versionen

XInput ist eine plattformübergreifende API, die zur Verwendung auf Xbox und Windows ausgeliefert wurde. Auf Xbox wird XInput als statische Bibliothek ausgeliefert, die in die ausführbare Hauptdatei des Spiels kompiliert wird. Auf Windows wird XInput als DLL bereitgestellt, die in den Systemordnern des Betriebssystems installiert ist.

Es gibt derzeit drei aktuelle Versionen der XInput-DLL. Wählen Sie die entsprechende Version von XInput basierend auf der Funktionalität von XInput, die Sie verwenden, und den Versionen von Windows aus, die Sie unterstützen möchten.

- XInput 1.4: XInput 1.4 wird als Teil der Windows 10. Verwenden Sie diese Version zum Erstellen von UWP-Apps.
- XInput 9.1.0: XInput 9.1.0 wird als Teil von Windows Vista, Windows 7 und Windows 8 ausgeliefert. Verwenden Sie diese Version, wenn Ihre Desktop-App auf diesen Versionen von Windows ausgeführt werden soll und Sie grundlegende XInput-Funktionen verwenden.
- XInput 1.3: XInput 1.3 wird als verteilbare Komponente im DirectX SDK mit Unterstützung für Windows Vista, Windows 7 und Windows 8 ausgeliefert. Verwenden Sie diese Version, wenn Ihre Desktop-App auf diesen Versionen von Windows ausgeführt werden soll und Sie Funktionen benötigen, die von XInput 9.1.0 nicht unterstützt werden.

## <a name="xinput-14"></a>XInput 1.4

XInput 1.4 wird heute als Systemkomponente in Windows 8 als XINPUT1-4.DLL \_ ausgeliefert. Sie ist im Posteingang verfügbar und erfordert keine Neuverteilung mit einer Anwendung. Das Windows Software Development Kit (SDK) enthält den Header und die Importbibliothek für die statische Verknüpfung mit \_ XINPUT1-4.DLL. Informationen zum Herunterladen des Windows 8 SDK finden Sie unter [Downloads für die Entwicklung von Desktop-Apps.](https://developer.microsoft.com/windows/downloads/)

XInput 1.4 bietet diese hauptvorteile gegenüber anderen Versionen von XInput:

-   Dies ist die einzige Version, die in C++/DirectX Windows Store-Apps verwendet werden kann.
-   Die neue [**XInputGetAudioDeviceIds-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) stellt eine ID-Zeichenfolge für Audiogeräte bereit, mit der Sie eine XAudio2-Masteringstimme oder ein Audiogerät für ein Headset öffnen können, das an einen allgemeinen Xbox-Controller angefügt ist. Die [**XInputGetDSoundAudioDeviceGuids-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) ist in dieser Version nicht verfügbar.
-   Bietet verbesserte Gerätefunktionen, einschließlich XINPUT \_ CAPS \_ WIRELESS, XINPUT \_ CAPS \_ FFB \_ SUPPORTED, XINPUT \_ CAPS \_ PMD \_ SUPPORTED und XINPUT \_ CAPS NO NAVIGATION \_ \_ Flags und genauere Berichte zu XINPUT \_ CAPS VOICE \_ \_ SUPPORTED. Diese Flags werden im **Flags-Member** der [**XINPUT \_ CAPABILITIES-Struktur**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) kombiniert. Die [**XInputGetCapabilities-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) gibt **XINPUT \_ CAPABILITIES** zurück.

### <a name="xinput-910"></a>XInput 9.1.0

Wie XInput 1.4 wird XInput 9.1.0 heute als Systemkomponente in Windows 10, Windows 8.x, Windows 7 und Windows Vista als XINPUT9 \_ 1 \_0.DLL ausgeliefert. Sie wird hauptsächlich aus Gründen der Abwärtskompatibilität mit vorhandenen Anwendungen beibehalten. Da es einen reduzierten Funktionssatz gibt, wird empfohlen, nach Möglichkeit XInput 1.4 zu verwenden. Es ist jedoch praktisch, für Anwendungen zu verwenden, die auf downleveln Versionen von Windows ausgeführt werden müssen, aber nicht die zusätzliche Audiofunktionalität von XInput 1.4 oder XInput 1.3 benötigen.

Das Windows SDK enthält den Header und die Importbibliothek für die statische Verknüpfung mit XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 hat diese Nachteile gegenüber anderen Versionen von XInput:

-   Aus Gründen der Abwärtskompatibilität gibt [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) in dieser Version von XInput feste Funktionsinformationen zurück. **XInputGetCapabilities** in XInput 9.1.0 meldet immer einen Geräteuntertyp von GAMEPAD, unabhängig davon, ob ein Xbox-Gerät mit einem allgemeinen Controller angeschlossen ist. Das XINPUT \_ CAPS WIRELESS-Funktionsbit wird auch dann nicht \_ zurückgegeben, wenn ein Drahtlosgerät verbunden ist.
-   Sie können das Headset für eine bestimmte Benutzer-ID nicht bestimmen. Die [**XInputGetAudioDeviceIds-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) ist nicht verfügbar, und die [**XInputGetDSoundAudioDeviceGuids-Funktion**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) gibt keine Ergebnisse für Windows 8.x oder Windows 10 zurück.
-   Die Funktionen [**XInputEnable,**](/windows/desktop/api/XInput/nf-xinput-xinputenable) [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)und [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) sind nicht verfügbar.

### <a name="xinput-13"></a>XInput 1.3

Einige frühere Versionen von XInput wurden als verteilbare DLLs im DirectX SDK bereitgestellt. Die erste verteilbare Version von XInput, XInput 1.1, wurde im April 2006-Release des DirectX SDK ausgeliefert. Die letzte im DirectX SDK zu liefernde Version war XInput 1.3, die im Juni 2010-Release des älteren DirectX SDK verfügbar war. *Das DirectX SDK ist unter Microsoft Downloads nicht mehr verfügbar.*

Sie können XInput 1.3 für Anwendungen verwenden, die Downlevelversionen von Windows unterstützen und Funktionen erfordern, die nicht von XInput 9.1.0 bereitgestellt werden (d.h. korrekte Untertypberichterstellung, Audiounterstützung, explizite Akkuberichtsunterstützung usw.).
