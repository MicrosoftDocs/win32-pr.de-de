---
description: Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsrelevante Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Generierung von Überwachungsdatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362706"
---
# <a name="audit-generation"></a>Generierung von Überwachungsdatensätzen

Sicherheitsanforderungen auf C2-Ebene geben an, dass Systemadministratoren in der Lage sein müssen, sicherheitsrelevante Ereignisse zu überwachen, und dass der Zugriff auf diese Überwachungsdaten auf autorisierte Administratoren beschränkt werden muss. Die Windows-API stellt Funktionen bereit, mit denen Administratoren sicherheitsrelevante Ereignisse überwachen können.

Die Sicherheits Beschreibung für ein Sicherungs fähiges Objekt kann eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) haben. Eine SACL enthält [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs), die die Typen der Zugriffsversuche angeben, mit denen Überwachungsberichte generiert werden. Jeder ACE identifiziert einen Vertrauens nehmer, einen Satz von Zugriffsrechten und einen Satz von Flags, die angeben, ob das System Überwachungs Meldungen für fehlgeschlagene Zugriffsversuche, erfolgreiche Zugriffsversuche oder beides generiert.

Das System schreibt Überwachungs Meldungen in das Sicherheits Ereignisprotokoll. Informationen zum Zugreifen auf die Datensätze in einem Sicherheits Ereignisprotokoll finden Sie unter [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging).

Um die SACL eines Objekts zu lesen oder zu schreiben, muss ein Thread zunächst die \_ Berechtigung "SE Security Name" aktivieren \_ . Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](sacl-access-right.md).

Die Windows-API bietet auch Unterstützung für Server Anwendungen zum Generieren von Überwachungs Meldungen, wenn ein Client versucht, auf ein privates Objekt zuzugreifen. Weitere Informationen finden Sie unter Überwachen des [Zugriffs auf private Objekte](auditing-access-to-private-objects.md).

 

 
