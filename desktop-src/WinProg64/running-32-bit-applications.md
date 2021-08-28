---
title: Ausführen von 32-Bit-Anwendungen
description: Führen Sie 32-Bit Windows-basierten Anwendungen nahtlos auf 64-Bit-Windows mit dem WOW64 x86-Emulator aus. Außerdem erfahren Sie mehr über den Registrierungs director, dateisystem redirector, die Anwendungsinstallation auf 64-Bit-Systemen und das Debuggen von WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- WOW64-64-Bit-Windows Programmierung
- WOW64 64-Bit-Windows Programmierung , informationen zu
- 32-Bit-Anwendungen auf 64-Bit-Windows 64-Bit-Windows Programmieren
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows , WOW64 Siehe WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1da192f4109afe09133f036d5fff88e772bbcc2c7d20ceb456e3233ab2b60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132823"
---
# <a name="running-32-bit-applications"></a>Ausführen von 32-Bit-Anwendungen

WOW64 ist der x86-Emulator, mit dem 32-Bit-Windows-basierte Anwendungen nahtlos auf 64-Bit-Windows. Dadurch können 32-Bit-Anwendungen (x86) Windows-Anwendungen nahtlos in 64-Bit-Anwendungen (x64) Windows sowie 32-Bit-Anwendungen (x86) und 32-Bit-Anwendungen (ARM) Windows nahtlos in 64-Bit-Anwendungen (ARM64) Windows. WOW64 wird mit dem Betriebssystem bereitgestellt und muss nicht explizit aktiviert werden. Weitere Informationen finden Sie unter [WOW64-Implementierungsdetails.](wow64-implementation-details.md)

Das System isoliert 32-Bit-Anwendungen von 64-Bit-Anwendungen, was dazu gehört, Datei- und Registrierungskollisionen zu verhindern. Konsolen-, GUI- und Dienstanwendungen werden unterstützt. Das System bietet Interoperabilität über die 32/64-Grenze hinweg für Szenarien wie Ausschneiden und Einfügen und COM. 32-Bit-Prozesse können jedoch keine 64-Bit-DLLs für die Ausführung laden, und 64-Bit-Prozesse können keine 32-Bit-DLLs für die Ausführung laden. Diese Einschränkung gilt nicht für DLLs, die als Datendateien oder Bildressourcendateien geladen werden. Weitere Informationen finden Sie unter [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Eine 32-Bit-Anwendung kann erkennen, ob sie unter WOW64 ausgeführt wird, indem sie die [**IsWow64Process-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) aufruft (verwenden [**Sie IsWow64Process2,**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) wenn sie auf Windows 10). Die Anwendung kann mithilfe der [**GetNativeSystemInfo-Funktion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) zusätzliche Informationen zum Prozessor abrufen.

Beachten Sie, dass 64-Bit-Windows das Ausführen von 16-Bit-Windows-basierten Anwendungen nicht unterstützt. Der Hauptgrund ist, dass Handles 32 signifikante Bits auf 64-Bit-Windows. Daher können Handles nicht abgeschnitten und ohne Datenverlust an 16-Bit-Anwendungen übergeben werden. Beim Starten von 16-Bit-Anwendungen tritt der folgende Fehler auf: **ERROR \_ BAD EXE \_ \_ FORMAT**.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Leistung und Arbeitsspeicherverbrauch unter WOW64](performance-and-memory-consumption.md)
-   [WOW64-Implementierungsdetails](wow64-implementation-details.md)
-   [Registrierungsumleitung](registry-redirector.md)
-   [Dateisystem-Redirector](file-system-redirector.md)
-   [Speicherverwaltung](memory-management.md)
-   [Prozessoraffinität](processor-affinity.md)
-   [Prozessübergreifende Kommunikation](interprocess-communication.md)
-   [Anwendungsinstallation](application-installation.md)
-   [Debuggen von WOW64](debugging-wow64.md)

 

 