---
description: Das Windows SDK (WSDK) enthält drei vollständige Beispielleistungs-DLLs.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Leistungs-DLL-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94e77ed35b1c328879ad5f83dded45fe92bf4a62ae15c794e5d9d9b23daeda1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143883"
---
# <a name="performance-dll-samples"></a>Leistungs-DLL-Beispiele

Das Windows SDK (WSDK) enthält drei vollständige Beispielleistungs-DLLs. Diese Beispiele befinden sich im Verzeichnis Beispiele \\ winBase \\ WinNT \\ PerfTool \\ PerfDlls. Der Stamm dieses Pfads ist das Basisinstallationsverzeichnis des WSDK. Sie können das WSDK aus dem [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) herunterladen (suchen Sie nach Windows SDK, und wählen Sie den Download für das neueste veröffentlichte Betriebssystem aus).

In diesem Verzeichnis sind folgende Beispiele enthalten:

-   **AppMem**: Stellt Entsprechungen der Funktionen [**GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)und [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) bereit, die Leistungsinformationen melden. Leistungsindikatoren in der Registrierung und im Leistungstool können die Leistungsinformationen lesen.
-   **LeakyBin**– Veranschaulicht die Verwendung von Anwendungsleistungsindikatoren.
-   **PerfGen**: Stellt drei Wellenformen mit fünf verschiedenen Zeiträumen für die Verwendung mit dem Leistungstool bereit, um Daten mit einer bekannten Rate und einem bekannten Wert bereitzustellen. Dies kann beim Testen von Anwendungen nützlich sein, die Leistungsdaten verwenden und vorhersagbare Werte zum Testen benötigen.

 

 
