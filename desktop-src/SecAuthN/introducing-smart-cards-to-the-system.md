---
description: Bevor das Smartcardsubsystem eine Smartcard finden kann, muss die Smartcard in das System eingefügt werden.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Einführung in Smartcards für das System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217766"
---
# <a name="introducing-smart-cards-to-the-system"></a>Einführung in Smartcards für das System

Bevor das [*Smartcardsubsystem*](../secgloss/s-gly.md) eine [*Smartcard*](../secgloss/s-gly.md)finden kann, muss die Smartcard in das System eingefügt werden. Dies erfolgt in der Regel mit einem Smartcard-Setup Tool, das vom Kartenhersteller bereitgestellt wird. Das Tool könnte als Programm auf einer Diskette (mit der Smartcard), einem ActiveX-Steuerelement, das auf einer Website verfügbar ist, usw. stehen.

Das Setup Tool muss die folgenden Informationen zur Karte bereitstellen:

-   Die [*ATR-Zeichenfolge*](../secgloss/a-gly.md)und eine optionale Maske, die als Hilfe bei der Identifizierung der Karte verwendet werden soll.
-   Eine Liste der smartcardschnittstellen, die von der Karte unterstützt werden.
-   Ein Anzeige Name für die Karte, der zum Identifizieren der Karte für den Benutzer verwendet werden soll. In den meisten Fällen wird dies vom Benutzer für das Setup-Tool bereitgestellt.
-   Der [*primäre Dienstanbieter*](../secgloss/p-gly.md) , der der Karte (optional) zugeordnet ist und für den Zugriff auf die Karte über COM-Schnittstellen verwendet wird.

Zum Vereinfachen der Setup Tools und zur Gewährleistung der Integrität der [*smartcarddatenbank*](../secgloss/s-gly.md)bietet das Smartcard-Subsystem die folgenden zwei Funktionen. Mit " [**scardintroducecardtype**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) " wird eine Smartcard in die Datenbank eingeführt, und " [**scardforgetcardtype**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) " wird aus der Datenbank entfernt.

 

 
