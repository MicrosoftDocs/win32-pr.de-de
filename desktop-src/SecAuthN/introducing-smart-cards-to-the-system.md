---
description: Bevor das Smartcardsubsystem eine Smartcard finden kann, muss die Smartcard in das System eingeführt werden.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Einführung von Smartcards in das System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cd65135e1580792135a1042729f2002f4437697fa0548a4f6cd776650485b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015710"
---
# <a name="introducing-smart-cards-to-the-system"></a>Einführung von Smartcards in das System

Bevor das [*Smartcardsubsystem*](../secgloss/s-gly.md) eine Smartcard [*finden kann,*](../secgloss/s-gly.md)muss die Smartcard in das System eingeführt werden. Dies erfolgt in der Regel mit einem Smartcard-Setuptool, das vom Kartenhersteller bereitgestellt wird. Das Tool kann als Programm auf einer Diskette (mit der Smartcard), einem ActiveX steuerelement, das auf einer Website verfügbar ist, und so weiter.

Das Setuptool muss die folgenden Informationen zur Karte bereitstellen:

-   Die [*ATR-Zeichenfolge*](../secgloss/a-gly.md)und eine optionale Maske, die als Hilfe beim Identifizieren der Karte verwendet werden soll.
-   Eine Liste der von der Karte unterstützten Smartcardschnittstellen.
-   Ein Anzeigename für die Karte, der zum Identifizieren der Karte für den Benutzer verwendet werden soll. In den meisten Fällen wird dies vom Benutzer für das Setuptool zur Verfügung angezeigt.
-   Der [*primäre Dienstanbieter, der*](../secgloss/p-gly.md) der Karte zugeordnet ist (optional), der beim Zugriff auf die Karte über COM-Schnittstellen verwendet werden soll.

Um die Einrichtungstools zu vereinfachen und die Integrität der Smartcard-Datenbank [*sicherzustellen,*](../secgloss/s-gly.md)stellt das Smartcard-Subsystem die folgenden beiden Funktionen zur Verfügung. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) führt eine Smartcard in die Datenbank ein, und [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) entfernt sie aus der Datenbank.

 

 
