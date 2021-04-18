---
description: Im folgenden Verfahren wird beschrieben, wie die Debugverfolgung und Protokollierung aktiviert wird.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Aktivieren der Debugablaufverfolgung/Protokollierung für abgeleitete MSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3883d12c050f245cc58595c9a52586c4f01ba27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347249"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Aktivieren der Debugablaufverfolgung/Protokollierung für abgeleitete MSPs

Stellen Sie zunächst sicher, dass die Implementierung des abgeleiteten msp die Richtlinien im vorherigen Abschnitt im Hinblick auf die Debugablaufverfolgung befolgt hat (definieren des Präprozessorsymbols msplog, registrieren für die Ablauf Verfolgung während DllMain und Verwenden des Log-Makros für die Ablauf Verfolgung). Ermitteln Sie, welcher Name der MSP bei der Registrierung für die Ablauf Verfolgung verwendet (Dies sollte in der Regel der Name der DLL sein; er wird unten als " &lt; dll-Name &gt; " bezeichnet). Um die Ablauf Verfolgung zu aktivieren, verwenden Sie einen Registrierungs-Editor ("Regedit.exe" oder "Regedt32.exe"), um den Schlüssel "HKEY \_ local \_ Machine \\ Software \\ Microsoft Tracing" zu suchen, \\ und führen Sie die folgenden Schritte aus. Beachten Sie, dass alle unten erwähnten Werte, mit Ausnahme des enabledebugertracing-Werts, automatisch erstellt werden sollten, nachdem ihr MSP zum ersten Mal ausgeführt wurde.

-   Legen Sie den **DWORD** -Wert <dll name> enabledebuggertracing auf 1 fest, um die Ablauf Verfolgung für Debugger im Benutzer-und Kernelmodus zu aktivieren \\ . Verwenden Sie optional den **DWORD** -Wert <dll name> \\ consoletracing Mask zum Aktivieren oder deaktivieren verschiedener Ebenen der Ablauf Verfolgungs Ausgabe (der Standardwert ist 0xFFFF0000, wodurch alle Ablauf Verfolgungs Ebenen aktiviert werden).
-   Legen Sie für den **DWORD** -Wert <dll name> EnableFileTracing den Wert 1 fest, um die Ablauf Verfolgung für eine Datei zu aktivieren \\ . Verwenden Sie optional den Zeichen folgen Wert- <dll name> \\ Datei Verzeichnis, um den Speicherort der Protokolldatei anzupassen. Verwenden Sie optional den **DWORD** -Wert <dll name> \\ FileTracingMask, um verschiedene Ebenen der Ablauf Verfolgungs Ausgabe zu aktivieren oder zu deaktivieren (der Standardwert ist 0xFFFF0000, wodurch alle Ablauf Verfolgungs Ebenen aktiviert werden).
-   Legen Sie für den DWORD-Wert enableconsoletracing den **DWORD** -Wert enableconsoletracing auf 1 fest, und legen Sie für den **DWORD** -Wert <dll name> \\ enableconsoletracing den Wert 1 fest. Verwenden Sie optional den **DWORD** -Wert <dll name> \\ consoletracing Mask zum Aktivieren oder deaktivieren verschiedener Ebenen der Ablauf Verfolgungs Ausgabe (der Standardwert ist 0xFFFF0000, wodurch alle Ablauf Verfolgungs Ebenen aktiviert werden).

 

 



