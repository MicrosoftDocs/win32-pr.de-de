---
description: Erläutert die Mittel, mit denen eine Anwendung oder ein Dienstanbieter mithilfe des Smartcard-Subsystems eine Verbindung mit einer Smartcard herstellen kann.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Zugreifen auf eine Smartcard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ae7a7954d9a48191884c8ed0fd7ee65ad3bb007aae18b00efc6581e5f2e6221
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101470"
---
# <a name="accessing-a-smart-card"></a>Zugreifen auf eine Smartcard

Das [*Smartcardsubsystem*](/windows/desktop/SecGloss/s-gly) bietet einer Anwendung oder einem Dienstanbieter mehrere Möglichkeiten, [*eine*](/windows/desktop/SecGloss/c-gly) Verbindung mit einer Smartcard herzustellen:

-   Eine Anwendung kann [**SCardConnect aufrufen,**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) um eine Verbindung mit einer Karte herzustellen, die sich in einem bestimmten Reader befindet. Dies ist die einfachste Möglichkeit, die Kommunikation mit einer Smartcard zu herstellen.
-   Eine Anwendung kann innerhalb einer bestimmten Lesergruppe nach einer bestimmten Smartcard suchen. Die Anwendung identifiziert die Karte durch ihren Anzeigenamen und gibt eine Liste von Lesern an, in der die Karte angezeigt werden kann. Der [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) durchsucht die Liste der Leser nach Karten mit einer [*ATR-Zeichenfolge,*](/windows/desktop/SecGloss/a-gly) die der benannten Karte entspricht, und gibt Statusinformationen an die Anwendung zurück. Das [*Smartcardsubsystem*](/windows/desktop/SecGloss/s-gly) legt nie eine grafische Benutzeroberfläche auf oder interagiert mit der Karte, außer die ATR-Zeichenfolge zu erhalten. Sie liefert jedoch genügend Informationen, damit die Anwendung oder ein gemeinsames Steuerelement den Benutzer durch die Suche nach der gewünschten Karte oder dem gewünschten Kartentyp führt. Dies führt zur Zuordnung der Anforderung zu einem bestimmten Reader, an den weitere E/A-Anweisungen gerichtet werden.
-   Eine Anwendung kann eine Liste von Karten anfordern, die einen bestimmten Satz von Smartcardschnittstellen unterstützen. Die Anwendung kann dann die Liste im vorherigen Fall verwenden. Dadurch können Anwendungen basierend auf ihren Funktionen eine Verbindung mit Karten herstellen, ohne ihre Namen zu betrachten.

Wenn eine Anwendung nach einer Karte sucht, stellt sie ein Array von Readernamen zur Auswahl. Für jedes Readerelement im Array stellt der Ressourcen-Manager die folgenden Informationen zur Verfügung:

-   Gibt an, ob der Reader für diese Anwendung verfügbar ist.
-   Gibt an, ob eine Karte in diesen Reader eingefügt wird und wenn ja, wie die ATR-Zeichenfolge ist.
-   Gibt an, ob die ATR-Zeichenfolge der Karte mit einer der ATR-Zeichenfolgen der angeforderten Karte entspricht.

Die Anwendung verwendet die zurückgegebenen Informationen, um weitere Filter auf die Karten anzuwenden oder den Benutzer zur Auswahl der gewünschten Karte aufforderungen. Beachten Sie, dass eine oder mehrere der zurückgegebenen Readerlisten möglicherweise für die exklusive Verwendung durch andere Anwendungen geöffnet werden, sodass der Zugriff auf diese Leserliste nicht garantiert ist.

 

 
