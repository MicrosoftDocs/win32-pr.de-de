---
description: Im folgenden Verfahren wird beschrieben, wie Sie die Debugablaufverfolgung und -protokollierung aktivieren.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Aktivieren der Debugablaufverfolgung/-protokollierung für abgeleitete MSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140523"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Aktivieren der Debugablaufverfolgung/-protokollierung für abgeleitete MSPs

Stellen Sie zunächst sicher, dass die Implementierung des abgeleiteten MSP die Richtlinien im vorherigen Abschnitt in Bezug auf die Debugablaufverfolgung befolgt hat (Definieren des Präprozessorsymbols MSPLOG, Registrierung für die Ablaufverfolgung während DllMain und Verwenden des LOG-Makros für die Ablaufverfolgung). Finden Sie heraus, welchen Namen der MSP bei der Registrierung für die Ablaufverfolgung verwendet (dies sollte in der Regel der Name der DLL sein, der unten als &lt; "DLL-Name" bezeichnet &gt; wird). Verwenden Sie zum Aktivieren der Ablaufverfolgung einen Registrierungs-Editor ("Regedit.exe" oder "Regedt32.exe"), um den Schlüssel "HKEY LOCAL MACHINE Software Microsoft Tracing" zu suchen, und gehen \_ \_ Sie wie folgt \\ \\ \\ vor. Beachten Sie, dass alle unten genannten Werte mit Ausnahme des EnableDebuggerTracing-Werts automatisch erstellt werden sollten, nachdem Sie Ihren MSP zum ersten Mal ausgeführt haben.

-   Um die Ablaufverfolgung für Debugger im Benutzer- und Kernelmodus zu aktivieren, legen Sie **den DWORD-Wert** <dll name> \\ EnableDebuggerTracing auf 1 fest. Verwenden Sie optional den **DWORD-Wert** ConsoleTracing Mask, um verschiedene Ebenen der Ablaufverfolgungsausgabe zu aktivieren oder zu deaktivieren (der Standardwert ist 0xFFFF0000, wodurch alle <dll name> \\ Ablaufverfolgungsebenen aktiviert werden).
-   Um die Ablaufverfolgung für eine Datei zu aktivieren, legen Sie **den DWORD-Wert** <dll name> \\ EnableFileTracing auf 1 fest. Verwenden Sie optional den Zeichenfolgenwert <dll name> \\ FileDirectory, um den Speicherort der Protokolldatei anzupassen. Verwenden Sie optional den **DWORD-Wert** <dll name> FileTracingMask, um verschiedene Ebenen der Ablaufverfolgungsausgabe zu aktivieren oder zu deaktivieren (der Standardwert ist 0xFFFF0000, wodurch alle Ablaufverfolgungsebenen \\ aktiviert werden).
-   Um die Ablaufverfolgung in einem separaten Konsolenfenster zu aktivieren, das durch eine DLL getrennt ist, legen Sie den **DWORD-Wert** EnableConsoleTracing auf 1 und außerdem den **DWORD-Wert** <dll name> \\ EnableConsoleTracing auf 1 fest. Verwenden Sie optional den **DWORD-Wert** ConsoleTracing Mask, um verschiedene Ebenen der Ablaufverfolgungsausgabe zu aktivieren oder zu deaktivieren (der Standardwert ist 0xFFFF0000, wodurch alle <dll name> \\ Ablaufverfolgungsebenen aktiviert werden).

 

 



