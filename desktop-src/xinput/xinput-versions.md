---
title: Xinput-Versionen
description: Xinput ist eine plattformübergreifende API, die für die Verwendung auf Xbox und Windows ausgeliefert wurde.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d3624b8ea12872058ed1d874aa242a5806aec2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "103869396"
---
# <a name="xinput-versions"></a>Xinput-Versionen

Xinput ist eine plattformübergreifende API, die für die Verwendung auf Xbox und Windows ausgeliefert wurde. Auf der Xbox wird xinput als statische Bibliothek ausgeliefert, die in die ausführbare Datei des Hauptspiels kompiliert wird. Unter Windows wird xinput als DLL bereitgestellt, die in den Systemordnern des Betriebssystems installiert ist.

Zurzeit gibt es drei aktuelle Versionen der xinput-dll. Wählen Sie die entsprechende Version von xinput basierend auf der Funktionalität von xinput, die Sie verwenden, und den Versionen von Windows aus, die Sie unterstützen möchten.

- Xinput 1,4: xinput 1,4 wird als Teil von Windows 10 ausgeliefert. Verwenden Sie diese Version zum Entwickeln von UWP-apps.
- Xinput 9.1.0: xinput 9.1.0 wird als Teil von Windows Vista, Windows 7 und Windows 8 ausgeliefert. Verwenden Sie diese Version, wenn Ihre Desktop-app in diesen Versionen von Windows ausgeführt werden soll und Sie grundlegende xinput-Funktionen verwenden.
- Xinput 1,3: xinput 1,3 wird als verteilbare Komponente im DirectX SDK mit Unterstützung für Windows Vista, Windows 7 und Windows 8 ausgeliefert. Verwenden Sie diese Version, wenn Ihre Desktop-app in diesen Versionen von Windows ausgeführt werden soll und Sie Funktionalität benötigen, die von xinput 9.1.0 nicht unterstützt wird.

## <a name="xinput-14"></a>Xinput 1,4

Xinput 1,4 wird heute als Systemkomponente in Windows 8 als XINPUT1- \_4.DLL ausgeliefert. Es ist "Inbox" verfügbar und erfordert keine Neuverteilung mit einer Anwendung. Das Windows Software Development Kit (SDK) enthält den Header und die Import Bibliothek für die statische Verknüpfung mit XINPUT1- \_4.DLL. Informationen zum Herunterladen des Windows 8 SDK finden Sie unter [Downloads für die Entwicklung von Desktop-Apps](https://developer.microsoft.com/windows/downloads/).

Xinput 1,4 bietet diese Hauptvorteile gegenüber anderen Versionen von xinput:

-   Dies ist die einzige Version, die in C++/DirectX Windows Store-Apps verwendet werden kann.
-   Die neue Funktion " [**xinputgetaudiodebug**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) " stellt eine ID-Zeichenfolge für das Audiogerät bereit, die Sie verwenden können, um ein XAudio2 Mastering Voice-oder Audiogerät für ein an einen Xbox Common Controller angefügtes Headset zu öffnen. Die Funktion " [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) " ist in dieser Version nicht verfügbar.
-   Bietet verbesserte Geräte Funktions Berichte, einschließlich xinput \_ Caps \_ Wireless, xinput \_ Caps \_ FFB \_ supported, xinput \_ Caps \_ PMD \_ wird unterstützt, und xinput \_ Caps \_ keine \_ navigationflags und genauere Berichterstellung für die \_ unterstützte xinput Caps- \_ Sprache \_ . Diese Flags werden im **Flags** -Member der [**xinput- \_ Funktionen**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) -Struktur kombiniert. Die Funktion " [**xinputgetfunctions**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) " gibt **xinput- \_ Funktionen** zurück.

### <a name="xinput-910"></a>Xinput 9.1.0

Wie xinput 1,4 ist xinput 9.1.0 heute als Systemkomponente in Windows 10, Windows 8. x, Windows 7 und Windows Vista als XINPUT9 \_ 1-0.DLL ausgeliefert \_ . Sie wird hauptsächlich aus Gründen der Abwärtskompatibilität mit vorhandenen Anwendungen beibehalten. Die Funktion verfügt über einen reduzierten Funktions Satz. Daher empfiehlt es sich, nach Möglichkeit xinput 1,4 zu verwenden. Es ist jedoch praktisch, für Anwendungen zu verwenden, die auf untergeordneten Versionen von Windows ausgeführt werden müssen, jedoch nicht die zusätzlichen Audiofunktionen benötigen, die von xinput 1,4 oder xinput 1,3 bereitgestellt werden.

Die Windows SDK enthält den Header und die Import Bibliothek für die statische Verknüpfung mit XINPUT9 \_ 1 \_0.DLL.

Xinput 9.1.0 hat diese Nachteile gegenüber anderen Versionen von xinput:

-   Aus Gründen der Abwärtskompatibilität gibt " [**xinputgetcapability**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) " in dieser Version von xinput Informationen zu festem Funktionsumfang zurück. Unabhängig vom angefügten Xbox Common Controller-Gerät meldet " **xinputgetfunktionalitäten** " in xinput 9.1.0 immer einen Geräte Untertyp von "Gamepad". Er gibt das drahtlos Funktions Bit von xinput Caps nicht zurück, \_ \_ auch wenn ein drahtlos Gerät angeschlossen ist.
-   Sie können das Headset für eine bestimmte Benutzer-ID nicht ermitteln. Die Funktion " [**xinputgetaudiodeviceids**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) " ist nicht verfügbar, und die Funktion " [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) " gibt keine Ergebnisse für Windows 8. x oder Windows 10 zurück.
-   Die Funktionen " [**xinputenable**](/windows/desktop/api/XInput/nf-xinput-xinputenable)", " [**xinputgetbatteryinformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)" und " [**xinputgetkeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) " sind nicht verfügbar.

### <a name="xinput-13"></a>Xinput 1,3

Einige frühere Versionen von xinput wurden als verteilbare DLLs im DirectX SDK bereitgestellt. Die erste verteilbare Version von xinput, xinput 1,1, ausgeliefert in der Version vom April 2006 des DirectX SDK. Die letzte Version, die im DirectX SDK ausgeliefert werden soll, war xinput 1,3, verfügbar in der Version vom Juni 2010 des Legacy-DirectX SDK. *Das DirectX SDK ist nicht mehr in Microsoft-Downloads verfügbar*.

Sie können xinput 1,3 für Anwendungen verwenden, die untergeordnete Versionen von Windows unterstützen und Funktionen erfordern, die nicht von xinput 9.1.0 bereitgestellt werden (d. h. die korrekte unter typbericht Erstellung, Audiounterstützung, explizite Unterstützung von Akku Berichten usw.).
