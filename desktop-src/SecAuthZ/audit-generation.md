---
description: Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsbezogene Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generierung von Überwachungsdatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb2c6ab4b43d169e1ca6f6317489921987d22b507489ef0a5fd289d8483c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784696"
---
# <a name="audit-generation"></a>Generierung von Überwachungsdatensätzen

Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsbezogene Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss. Die Windows-API stellt Funktionen bereit, mit denen ein Administrator sicherheitsbezogene Ereignisse überwachen kann.

Der Sicherheitsdeskriptor für ein sicherungsfähiges Objekt kann über eine [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) verfügen. Eine SACL enthält [*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (Access Control Entries, ACEs), die die Typen von Zugriffsversuchen angeben, die Überwachungsberichte generieren. Jeder ACE identifiziert einen Vertrauenshänder, einen Satz von Zugriffsrechten und einen Satz von Flags, die angeben, ob das System Überwachungsmeldungen für fehlgeschlagene Zugriffsversuche, erfolgreiche Zugriffsversuche oder beides generiert.

Das System schreibt Überwachungsmeldungen in das Sicherheitsereignisprotokoll. Informationen zum Zugriff auf die Datensätze in einem Sicherheitsereignisprotokoll finden Sie unter [Ereignisprotokollierung.](/windows/desktop/EventLog/event-logging)

Um die SACL eines Objekts zu lesen oder zu schreiben, muss ein Thread zuerst die Berechtigung SE \_ SECURITY \_ NAME aktivieren. Weitere Informationen finden Sie unter [SACL Access Right](sacl-access-right.md).

Die Windows-API bietet auch Unterstützung für Serveranwendungen zum Generieren von Überwachungsmeldungen, wenn ein Client versucht, auf ein privates Objekt zuzugreifen. Weitere Informationen finden Sie unter [Überwachen des Zugriffs auf private Objekte.](auditing-access-to-private-objects.md)

 

 
