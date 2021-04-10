---
description: Listet die Zuständigkeiten von Gina auf und erläutert diese.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Zuständigkeiten von Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042220"
---
# <a name="responsibilities-of-the-gina"></a>Zuständigkeiten von Gina

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Eine [*Gina*](../secgloss/g-gly.md) -dll besteht aus den folgenden Zuständigkeiten:

-   SAS-Überwachung

    Die Gina ist dafür verantwortlich, eine Sicherheits-und Überwachungs [*Sequenz*](../secgloss/s-gly.md) zu erkennen, SAS-Ereignisse zu überwachen und die Winlogon-Benachrichtigung zu benachrichtigen, wenn eine SAS aufgetreten ist. Beachten Sie, dass mehr als eine SAS definiert werden kann, und dass sich der Satz definierter SASs im Laufe der Zeit ändern kann. Beispielsweise kann eine Gruppe von SASs vorhanden sein, wenn sich die [*Winlogon*](../secgloss/w-gly.md) -Datei im abgelegten Zustand befindet, und eine andere Gruppe, wenn Sie sich im angemeldeten Zustand befindet.

    Winlogon bietet Dienste zur Unterstützung von Gina in der Verwendung von STRG + ALT + ENTF-SAS.

-   SAS-Verarbeitung

    Ein Grund dafür, dass die Gina austauschbar ist, besteht darin, Alternative Identifikations-und Authentifizierungsmechanismen bereitzustellen. Zu diesem Zweck muss die Gina Alle Benutzeroberflächen präsentieren, die sich aus der Erkennung einer SAS ergeben. Wenn kein Benutzer angemeldet ist, ist die Gina dafür verantwortlich, Identifikations-und Authentifizierungs Optionen sowie alle anderen zulässigen Optionen, die nicht authentifiziert sind, zu präsentieren. Wenn ein Benutzer angemeldet ist, ist die Gina dafür zuständig, die relevanten Optionen für den Benutzer darzustellen und die entsprechenden Aktionen zu Unternehmen. Beispielsweise kann es in einem System, das eine [*Smartcard*](../secgloss/s-gly.md)enthält, sinnvoll sein, die Arbeitsstation automatisch zu sperren, wenn der Benutzer die Smartcard entfernt.

-   Shellaktivierung

    Wenn sich ein Benutzer anmeldet, ist die Gina für das Erstellen eines oder mehrerer anfänglicher Prozesse für diesen Benutzer verantwortlich. (In dieser Dokumentation wird davon ausgegangen, dass diese anfänglichen Prozesse eine Schnittstelle für den Benutzer darstellen. Dabei kann es sich jedoch um Prozesse handeln, die nicht notwendigerweise mit dem Benutzer interagieren müssen.) Diese Prozesse werden als *Benutzershell* oder nur als *Shell* bezeichnet. Im Rahmen der shellaktivierung muss die Gina das Token des neu angemeldeten Benutzers den Prozessen zuweisen. Winlogon bietet einen Dienst, der Gina beim Zuweisen des Tokens unterstützt.

 

 
