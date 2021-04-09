---
title: Ausführen von 32-Bit-Anwendungen
description: Führen Sie Windows-basierte 32-Bit-Anwendungen nahtlos auf 64-Bit-Fenstern mit dem WOW64 x86-Emulator aus. Außerdem erfahren Sie mehr über den Registry Director, den Dateisystem-Redirector, die Anwendungs Installation auf 64-Bit-Systemen und das Debuggen von WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- WOW64 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Informationen zu
- 32-Bit-Anwendungen auf 64-Bit Windows 64-Bit Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, WOW64 siehe WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948794"
---
# <a name="running-32-bit-applications"></a>Ausführen von 32-Bit-Anwendungen

WOW64 ist der x86-Emulator, der es ermöglicht, Windows-basierte 32-Bit-Anwendungen nahtlos auf 64-Bit-Fenstern auszuführen. Dadurch können 32-Bit-Windows-Anwendungen (x86) nahtlos in 64-Bit (x64)-Fenstern und für 32-Bit-(x86) und 32-Bit (Arm)-Windows-Anwendungen ausgeführt werden, um Sie nahtlos in ARM64-Fenstern (64 Bit) auszuführen. WOW64 wird mit dem Betriebssystem bereitgestellt und muss nicht explizit aktiviert werden. Weitere Informationen finden Sie unter [WOW64-Implementierungs Details](wow64-implementation-details.md).

Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, einschließlich der Vermeidung von Datei-und Registrierungs Kollisionen. Konsolen-, GUI-und Dienst Anwendungen werden unterstützt. Das System stellt Interoperabilität zwischen der 32/64-Grenze für Szenarien wie Ausschneiden, einfügen und com bereit. Allerdings können 32-Bit-Prozesse keine 64-Bit-DLLs für die Ausführung laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs für die Ausführung laden. Diese Einschränkung gilt nicht für DLLs, die als Datendateien oder Bild Ressourcen Dateien geladen werden. Weitere Informationen finden Sie unter [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Eine 32-Bit-Anwendung kann erkennen, ob Sie unter WOW64 durch Aufrufen der [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) -Funktion ausgeführt wird (verwenden Sie [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) , wenn Windows 10 als Zielversion verwendet wird). Die Anwendung kann zusätzliche Informationen über den Prozessor mithilfe der [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) -Funktion abrufen.

Beachten Sie, dass 64-Bit-Windows die Ausführung von 16-Bit-Windows-basierten Anwendungen nicht unterstützt. Der Hauptgrund ist, dass Handles 32 signifikante Bits auf 64-Bit-Fenstern aufweisen. Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übermittelt werden. Der Versuch, 16-Bit-Anwendungen zu starten, schlägt mit folgendem Fehler fehl: **fehlerhafte \_ exe- \_ \_ Format**.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Leistung und Arbeitsspeicher Verbrauch unter WOW64](performance-and-memory-consumption.md)
-   [WOW64-Implementierungs Details](wow64-implementation-details.md)
-   [Registrierungs Redirector](registry-redirector.md)
-   [Datei System-Redirector](file-system-redirector.md)
-   [Speicherverwaltung](memory-management.md)
-   [Prozessoraffinität](processor-affinity.md)
-   [Prozessübergreifende Kommunikation](interprocess-communication.md)
-   [Anwendungs Installation](application-installation.md)
-   [Debuggen WOW64](debugging-wow64.md)

 

 