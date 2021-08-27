---
description: Listet die Zuständigkeiten der GINA auf und erläutert sie.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Zuständigkeiten der GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e4d2189d1d4258566a5e4baab357dc446a8f1c4ea409d7af328a85bf84c217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919038"
---
# <a name="responsibilities-of-the-gina"></a>Zuständigkeiten der GINA

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Eine [*GINA-DLL*](../secgloss/g-gly.md) hat die folgenden Aufgaben:

-   SAS-Überwachung

    Die GINA ist dafür verantwortlich, eine [*sichere Aufmerksamkeitssequenz (Secure Attention Sequence,*](../secgloss/s-gly.md) SAS) zu erkennen, SAS-Ereignisse zu überwachen und Winlogon zu benachrichtigen, wenn eine SAS aufgetreten ist. Beachten Sie, dass mehrere SAS definiert sein können und sich der Satz der definierten SAS im Laufe der Zeit ändern kann. Es kann z. B. eine Gruppe von SASs geben, wenn [*Winlogon*](../secgloss/w-gly.md) den Status "Abgemeldet" aufwies, und einen anderen Satz, wenn er sich im Status "Angemeldet" befindet.

    Winlogon bietet Dienste zur Unterstützung der GINA bei der Verwendung der SAS STRG+ALT+ENTF.

-   SAS-Verarbeitung

    Ein Grund für die Ersetzung der GINA ist die Bereitstellung alternativer Identifikations- und Authentifizierungsmechanismen. Hierzu muss die GINA alle Benutzeroberflächen anzeigen, die sich aus der Erkennung einer SAS ergeben. Wenn kein Benutzer angemeldet ist, ist die GINA für die Darstellung von Identifikations- und Authentifizierungsoptionen sowie aller anderen zulässigen Optionen verantwortlich, die nicht authentifiziert sind. Wenn ein Benutzer angemeldet ist, ist die GINA dafür verantwortlich, dem Benutzer die relevanten Optionen zu präsentieren und alle Aktionen durchzuführen, die als angemessen eingestuft werden. In einem System, das eine [*Smartcard*](../secgloss/s-gly.md)enthält, kann es beispielsweise sinnvoll sein, die Arbeitsstation automatisch zu sperren, wenn der Benutzer die Smartcard entfernt.

-   Shellaktivierung

    Wenn sich ein Benutzer anmeldet, ist die GINA dafür verantwortlich, einen oder mehrere anfängliche Prozesse für diesen Benutzer zu erstellen. (In dieser Dokumentation wird davon ausgegangen, dass diese anfänglichen Prozesse eine Schnittstelle für den Benutzer darstellen. Die Prozesse können jedoch tatsächlich alle Prozesse sein und müssen nicht unbedingt mit dem Benutzer interagieren.) Diese Prozesse werden als *Benutzershell* oder einfach als *Shell* bezeichnet. Im Rahmen der Shellaktivierung muss die GINA den Prozessen das Token des neu angemeldeten Benutzers zuweisen. Winlogon stellt einen Dienst bereit, der die GINA bei der Zuweisung des Tokens unterstützt.

 

 
