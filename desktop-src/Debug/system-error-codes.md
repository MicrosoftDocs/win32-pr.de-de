---
description: Stellt Links zu Systemfehlercodes bereit, die in der Headerdatei "WinError.h" definiert sind und für Entwickler vorgesehen sind.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Systemfehlercodes
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 4c762b2098531ecb19ad84522f8c9c8272c004397bbc4b32f15a6f6e157c4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691730"
---
# <a name="system-error-codes"></a>Systemfehlercodes

Dieser Abschnitt richtet sich an Entwickler, die Systemfehler debuggen. Wenn Sie diese Seite bei der Suche nach anderen Fehlern erreicht haben, finden Sie hier einige Links, die Ihnen helfen können:

* [Windows Updatefehler:](https://support.microsoft.com/help/10164/fix-windows-update-errors) Informationen zum Beheben von Problemen mit Windows Update.
* [Windows Aktivierungsfehler:](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) Sie können Ihre Kopie von Windows überprüfen.
* [Problembehandlung bei Bluescreenfehlern:](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) Hier finden Sie Hilfe bei der Ermittlung der Ursache eines Stoppfehlers.
* [Microsoft-Support:](https://support.microsoft.com) Support für ein Microsoft-Produkt.

## <a name="more-ways-to-find-an-error-code"></a>Weitere Möglichkeiten zum Suchen eines Fehlercodes

Wir haben die Systemfehlercodes in diesem Abschnitt nach Zahl geordnet aufgelistet. Wenn Sie weitere Hilfe beim Aufspüren eines bestimmten Fehlers benötigen, finden Sie hier einige weitere Empfehlungen:

* Verwenden Sie das [Microsoft-Tool für die Fehlersuche.](system-error-code-lookup-tool.md)
*  Installieren Sie die Debugtools für Windows, laden Sie eine Speicherabbilddatei, und führen Sie dann den **\! Fehlerbefehl \<code>** aus.
* Suchen Sie auf der Website Microsoft-Protokolle nach unformatiertem Text oder Fehlercode. Weitere Informationen finden Sie unter [[MS-ERREF]: Windows Fehlercodes](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Fehlercodes von Drittanbietern

Andere Fehlercodes können von Diensten oder Apps von Drittanbietern generiert werden (z. **B. Fehlercode: -118** kann vom [Game Service "Steam"](https://support.steampowered.com/kb_cat.php?id=59)angezeigt werden), und in diesen Situationen wenden Sie sich an die Supportzeile des Drittanbieters.

## <a name="system-error-codes"></a>Systemfehlercodes

Systemfehlercodes sind sehr weit gefasst: Jeder kann an einem von vielen Hundert Stellen im System auftreten. Daher können die Beschreibungen dieser Codes nicht sehr spezifisch sein. Die Verwendung dieser Codes erfordert ein gewisses Maß an Untersuchung und Analyse. Sie müssen sowohl den programmgesteuerten als auch den Laufzeitkontext notieren, in dem diese Fehler auftreten. 

Da diese Codes in WinError.h für alle Benutzer definiert sind, werden die Codes manchmal von Nicht-Systemsoftware zurückgegeben. Manchmal wird der Code von einer Funktion zurückgegeben, die sich tief im Stapel befindet und weit vom Code entfernt ist, der den Fehler behandelt.

Die folgenden Themen enthalten Listen mit Systemfehlercodes. Diese Werte werden in der Headerdatei WinError.h definiert.

-   [Systemfehlercodes (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Systemfehlercodes (500-999) (0x1f4-0x3e7)](system-error-codes--500-999-.md)
-   [Systemfehlercodes (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Systemfehlercodes (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Systemfehlercodes (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Systemfehlercodes (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Systemfehlercodes (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Systemfehlercodes (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Systemfehlercodes (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Systemfehlercodes (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
