---
description: Die Windows SDK (WSDK) enthält drei komplette Leistungs-DLLs für Stichproben.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Leistungs-DLL-Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358894"
---
# <a name="performance-dll-samples"></a>Leistungs-DLL-Beispiele

Die Windows SDK (WSDK) enthält drei komplette Leistungs-DLLs für Stichproben. Diese Beispiele befinden sich im Verzeichnis Samples \\ Winbase \\ Winnt \\ perftool \\ perfdlls. Der Stamm dieses Pfades ist das Basis Installationsverzeichnis des WSDK. Sie können das WSDK aus dem [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) herunterladen (suchen Sie nach Windows SDK, und wählen Sie den Download für das neueste veröffentlichte Betriebssystem aus).

Die in diesem Verzeichnis enthaltenen Beispiele sind:

-   **Appmem**– stellt Entsprechungen der Funktionen [**globalzugewiesenen**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**globalrezuweisung**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)und [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) bereit, die Leistungsinformationen melden. Leistungsindikatoren in der Registrierung und das Leistungs Tool können die Leistungsinformationen lesen.
-   " **Leakybin**–" veranschaulicht die Verwendung von Leistungsindikatoren für Anwendungen.
-   **Perfgen**– bietet drei Wellenformen in fünf verschiedenen Zeiträumen für die Verwendung mit dem Leistungs Tool, um Daten mit einer bekannten Geschwindigkeit und einem bekannten Wert bereitzustellen. Dies kann nützlich sein, um Anwendungen zu testen, die Leistungsdaten verwenden und vorhersagbare Werte für den Test benötigen.

 

 
