---
description: Eine geschützte Serveranwendung muss die Zugriffsrechte eines Clients überprüfen, bevor der Client den Zugriff auf ein geschütztes privates Objekt zulässt.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Überprüfen des Zugriffs auf private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959010"
---
# <a name="checking-access-to-private-objects"></a>Überprüfen des Zugriffs auf private Objekte

Eine geschützte Serveranwendung muss die Zugriffsrechte eines Clients überprüfen, bevor der Client den Zugriff auf ein geschütztes privates Objekt zulässt. Zu diesem Zweck übergibt der Server ein Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly), eine Sicherheits Beschreibung und einen Satz angeforderter Zugriffsrechte an [**Access Check**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). Die [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) in der DACL der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) geben die Zugriffsrechte an, die verschiedenen Treuhändern erteilt oder verweigert werden. Die **AccessCheck** -Funktion vergleicht den Treuhänder in jedem ACE mit den im Identitätswechsel Token identifizierten Treuhändern. Eine Beschreibung des Algorithmus, der verwendet wird, um den Zugriff zu gewähren oder zu verweigern, finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).

Die [**accesscheckandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) -Funktion führt eine ähnliche Zugriffs Überprüfung durch. Außerdem werden Überwachungsdaten Sätze im Sicherheits Ereignisprotokoll generiert, abhängig von der SACL in der Sicherheits Beschreibung.

Die [**accesscheckbytype**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) -und [**accesscheckbytypeandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) -Funktionen ähneln Access [**Check**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) und [**accesscheckandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , außer dass Sie den Zugriff auf die unter Objekte eines Objekts, z. b. Eigenschaften Sätze oder Eigenschaften, überprüfen können. Die Funktionen [**accesscheckbytyperesultlist**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) und [**accesscheckbytyperesultlistandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) sind auch mit **Access** Check vergleichbar, mit der Ausnahme, dass Sie die Ergebnisse der Zugriffs Überprüfung für jedes untergeordnete Objekt in einer Hierarchie der Eigenschaften und Eigenschaften Sätze des Objekts bereitstellen. Diese Funktionen verwenden die [**\_ \_ Listenstruktur Objekttyp**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) , um die Hierarchie von Objekten zu beschreiben, für die der Zugriff aktiviert ist. Die Funktionen, die eine Überwachungs Nachricht generieren, verwenden den Enumerationstyp [**Audit- \_ \_ Ereignistyp**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) , um anzugeben, ob das zu überprüfende Objekt ein Verzeichnisdienst Objekt ist. Weitere Informationen zur Hierarchie eines Objekts und dessen untergeordneten Elementen finden [Sie unter ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts](aces-to-control-access-to-an-object-s-properties.md).

Die angeforderten Zugriffsrechte, die an die Funktionen [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) und [**accesscheckandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) übermittelt wurden, dürfen keine [generischen Zugriffsrechte](generic-access-rights.md)enthalten. Der Server kann die [**mapgenericmask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) -Funktion verwenden, um alle generischen Zugriffsrechte entsprechend der in der [**generischen \_**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) Zuordnungs Struktur angegebenen Zuordnung in die entsprechenden spezifischen und Standardrechte zu konvertieren.

Die Funktionen [**areallaccessesgewährten**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) und [**areanyaccessesgewährten**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) vergleichen eine angeforderte [*Zugriffs Maske*](/windows/desktop/SecGloss/a-gly) mit einer gewährten Zugriffs Maske.

Beispielcode, der die [**Access Check**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Funktion verwendet, finden Sie unter [Überprüfen des Client Zugriffs mit ACLs in C++](verifying-client-access-with-acls-in-c--.md).

Die [**converttoautovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) -Funktion erstellt eine Sicherheits Beschreibung in einem Format, das die Automatische Propagierung von vererbbaren ACEs ermöglicht, und gibt Sie zurück. Diese Sicherheits Beschreibung enthält alle ACEs (geerbt und nongeerbt) in der aktuellen Sicherheits Beschreibung und ist in einem [*selbst relativen*](/windows/desktop/SecGloss/s-gly) Format enthalten. Die **converttoautovererprivateobjectsecurity** -Funktion bestimmt, ob die ACEs geerbt oder nicht geerbt werden, indem alle ACEs in der aktuellen Sicherheits Beschreibung mit allen ACEs in der übergeordneten Sicherheits Beschreibung verglichen werden. Zwischen den beiden Gruppen von ACEs besteht möglicherweise keine eins-zu-eins-Entsprechung. Beispielsweise kann ein ACE, der Lese-/Schreibberechtigung zulässt, zwei ACEs entsprechen: ein ACE, der Leseberechtigungen zulässt, und ein ACE, der die Schreib Berechtigung zulässt. Ein übergeordneter Sicherheits Deskriptor kann nicht bereitgestellt werden, wenn die aktuelle Sicherheits Beschreibung das übergeordnete Element ist.

 

 
