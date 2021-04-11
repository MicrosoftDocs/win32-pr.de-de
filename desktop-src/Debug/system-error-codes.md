---
description: Enthält Links zu Systemfehler Codes, die in der Header Datei "Winerror. h" definiert sind und für Entwickler gedacht sind.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: System Fehler Codes
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126829"
---
# <a name="system-error-codes"></a>System Fehler Codes

Dieser Abschnitt ist für Entwickler gedacht, die Systemfehler Debuggen. Wenn Sie diese Seite beim Suchen nach anderen Fehlern erreicht haben, finden Sie hier einige Links, die Ihnen helfen können:

* [Windows Update Fehler](https://support.microsoft.com/help/10164/fix-windows-update-errors) : Hilfe beim Beheben von Problemen mit Windows Update.
* [Windows-Aktivierungs Fehler](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) : Hilfe bei der Überprüfung Ihrer Kopie von Windows.
* Problembehandlung bei Problemen mit dem [blauen Bildschirm](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) : helfen Sie bei der Ermittlung der Ursache eines Fehlers.
* [Microsoft-Support](https://support.microsoft.com) für die Unterstützung eines Microsoft-Produkts.

## <a name="more-ways-to-find-an-error-code"></a>Weitere Möglichkeiten zum Auffinden eines Fehlercodes

Wir haben die Systemfehler Codes in diesem Abschnitt aufgeführt, geordnet nach Zahl. Wenn Sie weitere Hilfe bei der Nachverfolgung eines bestimmten Fehlers benötigen, finden Sie hier weitere Empfehlungen:

* Verwenden Sie das Microsoft-Tool für die [Fehlersuche](system-error-code-lookup-tool.md).
*  Installieren Sie die Debugtools für Windows, laden Sie eine Speicher Abbild Datei, und führen Sie dann den **\! Err \<code>** -Befehl aus.
* Suchen Sie auf der Microsoft-Protokoll Website nach dem unformatierten Text oder Fehlercode. Weitere Informationen finden Sie unter [[MS-erref]: Windows-Fehler Codes](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Fehlercodes von Drittanbietern

Andere Fehlercodes können von Drittanbieter Diensten oder-Apps generiert werden (z. b. **Fehler Code:-118** wird möglicherweise vom [Steam-Spiel Dienst](https://support.steampowered.com/kb_cat.php?id=59)angezeigt), und in diesen Fällen wenden Sie sich an die Support Abteilung von Drittanbietern.

## <a name="system-error-codes"></a>System Fehler Codes

System Fehler Codes sind sehr umfangreich: jede kann an einem von vielen Hunderten von Standorten im System auftreten. Folglich können die Beschreibungen dieser Codes nicht sehr spezifisch sein. Die Verwendung dieser Codes erfordert eine gewisse Untersuchung und Analyse. Sie müssen sowohl den programmgesteuerten als auch den Lauf Zeit Kontext berücksichtigen, in dem diese Fehler auftreten. 

Da diese Codes in WinError. h für alle Benutzer definiert sind, werden die Codes manchmal von nicht-Systemsoftware zurückgegeben. Manchmal wird der Code von einer Funktion, die tief im Stapel ist, und weit entfernt aus dem Code zurückgegeben, der den Fehler behandelt.

In den folgenden Themen finden Sie eine Liste der Systemfehler Codes. Diese Werte werden in der Header Datei "Winerror. h" definiert.

-   [System Fehler Codes (0-499) (0x0-0x1F)](system-error-codes--0-499-.md)
-   [System Fehler Codes (500-999) (0x1F 4-0x3e7)](system-error-codes--500-999-.md)
-   [System Fehler Codes (1000-1299) (0x3E8-0x513)](system-error-codes--1000-1299-.md)
-   [System Fehler Codes (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [System Fehler Codes (1700-3999) (0x6a4-0xF 9)](system-error-codes--1700-3999-.md)
-   [System Fehler Codes (4000-5999) (0xfa0-0x176 f)](system-error-codes--4000-5999-.md)
-   [System Fehler Codes (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [System Fehler Codes (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [System Fehler Codes (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [System Fehler Codes (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
