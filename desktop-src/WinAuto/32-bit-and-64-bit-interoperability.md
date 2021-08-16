---
title: 32-Bit- und 64-Bit-Interoperabilität
description: Hilfstechnologieanwendungen müssen über Prozessgrenzen hinweg kommunizieren, um Benutzeroberflächeninformationen von Microsoft Active Accessibility-Servern und Microsoft Benutzeroberflächenautomatisierung erhalten.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c056c9fe2792734e9369fa311e69528ce226f7edf15b82440b63c12c52de66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327989"
---
# <a name="32-bit-and-64-bit-interoperability"></a>32-Bit- und 64-Bit-Interoperabilität

Hilfstechnologieanwendungen müssen über Prozessgrenzen hinweg kommunizieren, um Benutzeroberflächeninformationen von Microsoft Active Accessibility-Servern und Microsoft Benutzeroberflächenautomatisierung erhalten. In diesem Thema werden die wichtigsten Probleme bei der prozessübergreifenden Kommunikation beschrieben, die Sie bei der Entwicklung Windows Barrierefreiheitsanwendungen berücksichtigen müssen.

Wenn Anwendungen die Windows Automation-API verwenden, behandeln die Microsoft Active Accessibility- und Benutzeroberflächenautomatisierung-Laufzeitkomponenten automatisch alle Probleme und Komplexitäten, die mit der Ausführung der prozessübergreifenden Kommunikation (Interprocess Communications, IPC) verbunden sind, einschließlich der Interoperabilitätsprobleme, die bei einem Prozess mit 32 Bits und einem anderen mit 64 Bits verbunden sind. Microsoft erkennt, dass eine Hilfstechnologieanwendung möglicherweise eine Form von IPC anstelle der Windows Automation-API verwenden muss, um mit einem Microsoft Active Accessibility-Server oder einem Benutzeroberflächenautomatisierung-Anbieter zu kommunizieren. In diesen Fällen empfiehlt Microsoft die Verwendung von DCOM- oder Windows-Nachrichten (nachrichten mit Werten, die kleiner als die von **WM \_ USER** sind), um mit anderen Prozessen zu kommunizieren. Wie die Windows Automation-API behandeln DCOM- und Windows-Nachrichten automatisch alle IPC-Probleme für Sie, einschließlich 32-Bit- bis 64-Bit-Interoperabilität.

Wenn die Windows Automation-API, DCOM und Windows keine Option sind, berücksichtigen Sie beim Implementieren der ausgewählten IPC-Methode die folgenden Probleme:

-   Gemeinsam genutzter Speicher– Beachten Sie bei Verwendung von freigegebenen Speicher, dass eine Struktur in einem 32-Bit-Prozess möglicherweise eine andere Größe und ein anderes Layout als die gleiche Struktur in einem 64-Bit-Prozess auf hat. Dies gilt insbesondere für Strukturen, die Zeiger oder Handles enthalten.
-   Zeigerverschneidung– Obwohl eine 32-Bit-Anwendung den **LONGLONG-Datentyp** zum Speichern eines 64-Bit-Werts verwenden kann, gibt es Instanzen, in denen kein Windows-API-Element vorhanden ist, die es der 32-Bit-Anwendung ermöglichen würden, einen 64-Bit-Wert aus einem 64-Bit-Prozess zu empfangen oder einen 64-Bit-Wert an einen 64-Bit-Prozess zu senden. Beispielsweise werden mit den [**Funktionen GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) und [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) alle Zeigerwerte abgeschnitten, und die 32-Bit-Anwendung wird mit einem wertlosen Wert belässt.
-   Handles– Da kernel32- und user32-Handles sowohl in 32-Bit- als auch in 64-Bit-Prozessen nur 32-Bit-Signifikant sind, können sie problemlos zwischen Prozessen übertragen werden. Einige Elemente, die Windows als Handles definiert werden, sind jedoch nur umschlossene Zeiger (z. B. **HTREEITEM**). Diese "Handles" werden abgeschnitten, wenn sie von einem 64-Bit-Prozess an einen 32-Bit-Prozess übergeben werden.
-   [WinEvent](winevents-infrastructure.md) Hookfunktionen– Um eine kontextspezifische Hookfunktion bei einem 32-Bit-Serverprozess zu registrieren, muss sich die Hookfunktion in einer 32-Bit-DLL befinden. Entsprechend muss sich die Hookfunktion in einer 64-Bit-DLL befinden, um eine Kontexthookfunktion bei einem 64-Bit-Serverprozess zu registrieren. Wenn eine Hilfstechnologieanwendung versucht, eine Kontexthookfunktion bei einem Server mit einer anderen Bittiefe zu registrieren, werden Ereignisse weiterhin an die Hookfunktion übermittelt, aber sie werden aus dem Kontext übermittelt. Weitere Informationen finden Sie unter WinEvents und [In-Context- und Out-of-Context-Hookfunktionen.](in-context-and-out-of-context-hook-functions.md)

Weitere Informationen zur 32-Bit- und 64-Bit-Interoperabilität finden Sie unter [Prozessinteroperabilität](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Übersicht über die Automation-API](windows-automation-api-overview.md)
</dt> </dl>

 

 