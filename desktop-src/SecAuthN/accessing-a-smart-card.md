---
description: Erläutert die Möglichkeiten, mit denen eine Anwendung oder ein Dienstanbieter mithilfe des Smartcard-Subsystems eine Verbindung mit einer Smartcard herstellen kann.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Zugreifen auf eine Smartcard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356209"
---
# <a name="accessing-a-smart-card"></a>Zugreifen auf eine Smartcard

Das [*Smartcard*](/windows/desktop/SecGloss/s-gly) -Subsystem bietet mehrere Möglichkeiten für eine Anwendung oder einen [*Dienstanbieter*](/windows/desktop/SecGloss/c-gly) , eine Verbindung mit einer Smartcard herzustellen:

-   Eine Anwendung kann [**scardconnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) zum Herstellen einer Verbindung mit einer Karte, die sich in einem bestimmten Reader befindet, aufruft. Dies ist die einfachste Möglichkeit, um eine Verbindung mit einer Smartcard herzustellen.
-   Eine Anwendung kann innerhalb einer bestimmten Gruppe von Lesern nach einer bestimmten Smartcard suchen. Die Anwendung identifiziert die Karte anhand ihres anzeigen Amens und gibt eine Liste von Lesern an, in der die Karte angezeigt werden kann. Der [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) durchsucht die Liste der Leser nach beliebigen Karten mit einer [*ATR-Zeichenfolge*](/windows/desktop/SecGloss/a-gly) , die mit der benannten Karte übereinstimmt, und gibt Statusinformationen an die Anwendung zurück. Das [*Smartcardsubsystem*](/windows/desktop/SecGloss/s-gly) stellt nie eine GUI her oder interagiert mit der Karte, die über das Abrufen der ATR-Zeichenfolge hinausgeht. Es werden jedoch genügend Informationen für die Anwendung oder ein gemeinsames Steuerelement bereitgestellt, um den Benutzer durch die Suche nach dem gewünschten Karten-oder Kartentyp durchlaufen zu können. Dies führt dazu, dass die Anforderung einem bestimmten Reader, an den weiter e/a weitergeleitet wird, entspricht.
-   Eine Anwendung kann eine Liste von Karten anfordern, die einen bestimmten Satz von smartcardschnittstellen unterstützt. Die Anwendung kann dann die Liste im vorherigen Fall verwenden. Dies ermöglicht es Anwendungen, die Verbindung mit Karten auf der Grundlage ihrer Funktionen ohne Berücksichtigung ihrer Namen herzustellen.

Wenn eine Anwendung nach einer Karte sucht, liefert Sie ein Array von Leser Namen, in denen gesucht werden soll. Der Ressourcen-Manager liefert für jedes Reader-Element im Array die folgenden Informationen:

-   Gibt an, ob der Reader für die Verwendung durch diese Anwendung verfügbar ist.
-   Gibt an, ob eine Karte in diesen Reader eingefügt wurde, und wenn ja, was die ATR-Zeichenfolge ist.
-   Gibt an, ob die ATR-Zeichenfolge der Karte mit den ATR-Zeichen folgen der angeforderten Karten übereinstimmt.

Die Anwendung verwendet die zurückgegebenen Informationen, um weitere Filter auf die Karten anzuwenden oder den Benutzer aufzufordern, die gewünschte Karte auszuwählen. Beachten Sie, dass mindestens eine der zurückgegebenen Readern für die ausschließliche Verwendung durch andere Anwendungen geöffnet werden kann, sodass der Zugriff auf diese Liste von Lesern nicht gewährleistet ist.

 

 
