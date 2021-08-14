---
description: Eine geschützte Serveranwendung muss die Zugriffsrechte eines Clients überprüfen, bevor der Client auf ein geschütztes privates Objekt zugreifen kann.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Überprüfen des Zugriffs auf private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f31f8ed05c16eed09cdd45da78f8fe58ecf41e283f6e6c37e7bc0480e63422d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783174"
---
# <a name="checking-access-to-private-objects"></a>Überprüfen des Zugriffs auf private Objekte

Eine geschützte Serveranwendung muss die Zugriffsrechte eines Clients überprüfen, bevor der Client auf ein geschütztes privates Objekt zugreifen kann. Hierzu übergibt der Server ein [*Identitätswechseltoken,*](/windows/desktop/SecGloss/i-gly)einen Sicherheitsdeskriptor und einen Satz angeforderter Zugriffsrechte an [**AccessCheck.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) Die [*Zugriffssteuerungseinträge (ACCESS Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) in der DACL des [*Sicherheitsdeskriptors*](/windows/desktop/SecGloss/s-gly) geben die Zugriffsrechte an, die verschiedenen Vertrauensnehmern gewährt oder verweigert werden. Die **AccessCheck-Funktion** vergleicht den Vertrauensnehmer in jedem ACE mit den Vertrauensnehmern, die im Identitätswechseltoken identifiziert wurden. Eine Beschreibung des Algorithmus, der zum Gewähren oder Verweigern des Zugriffs verwendet wird, finden Sie unter Steuern des Zugriffs auf ein Objekt durch [DACLs.](how-dacls-control-access-to-an-object.md)

Die [**AccessCheckAndAuditAlarm-Funktion**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) führt eine ähnliche Zugriffsüberprüfung durch. Darüber hinaus werden Überwachungsdatensätze im Sicherheitsereignisprotokoll generiert, abhängig von der SACL im Sicherheitsdeskriptor.

Die Funktionen [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) und [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) ähneln [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) und [**AccessCheckAndAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) mit der Ausnahme, dass Sie den Zugriff auf die Unterobjekte eines Objekts überprüfen können, z. B. Eigenschaftensätze oder Eigenschaften. Die Funktionen [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) und [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) ähneln auch **AccessCheck,** stellen jedoch die Ergebnisse der Zugriffsüberprüfung für jedes Unterobjekt in einer Hierarchie der Eigenschaften und Eigenschaftensätze des Objekts bereit. Diese Funktionen verwenden die [**OBJECT \_ TYPE \_ LIST-Struktur,**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) um die Hierarchie der Objekte zu beschreiben, für die der Zugriff überprüft wird. Die Funktionen, die eine Überwachungsmeldung generieren, verwenden den [**AUDIT \_ EVENT TYPE-Enumerationstyp, \_**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) um anzugeben, ob das überprüfte Objekt ein Verzeichnisdienstobjekt ist. Weitere Informationen zur Hierarchie eines Objekts und dessen Unterobjekten finden Sie unter [ACEs to Control Access to an Object es Properties](aces-to-control-access-to-an-object-s-properties.md).

Die angeforderten Zugriffsrechte, die an die Funktionen [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) und [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) übergeben werden, dürfen keine [generischen Zugriffsrechte](generic-access-rights.md)enthalten. Der Server kann die [**MapGenericMask-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) verwenden, um alle generischen Zugriffsrechte gemäß der in der [**GENERIC \_ MAPPING-Struktur**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) angegebenen Zuordnung in die entsprechenden spezifischen und Standardrechte zu konvertieren.

Die Funktionen [**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) und [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) vergleichen eine angeforderte [*Zugriffsmaske*](/windows/desktop/SecGloss/a-gly) mit einer gewährten Zugriffsmaske.

Beispielcode, der die [**AccessCheck-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) verwendet, finden Sie unter [Verifying Client Access with ACLs in C++ (Überprüfen des Clientzugriffs mit ACLs in C++).](verifying-client-access-with-acls-in-c--.md)

Die [**ConvertToAutoInheritPrivateObjectSecurity-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) erstellt und gibt einen Sicherheitsdeskriptor in einem Format zurück, das die automatische Weitergabe vererbbarer ACEs ermöglicht. Dieser Sicherheitsdeskriptor enthält alle geerbten und nicht geerbten ACEs im aktuellen Sicherheitsdeskriptor und weist ein [*selbst relatives*](/windows/desktop/SecGloss/s-gly) Format auf. Die **ConvertToAutoInheritPrivateObjectSecurity-Funktion** bestimmt, ob die ACEs geerbt werden oder nicht, indem alle ACEs im aktuellen Sicherheitsdeskriptor mit allen ACEs im übergeordneten Sicherheitsdeskriptor verglichen werden. Es gibt möglicherweise keine 1:1-Entsprechung zwischen den beiden AcEs-Gruppen. Beispielsweise kann ein ACE, der Lese-/Schreibberechtigungen zulässt, zwei ACEs entsprechen: einem ACE, der Leseberechtigungen zulässt, und einem ACE, der die Schreibberechtigung zulässt. Ein übergeordneter Sicherheitsdeskriptor wird möglicherweise nicht angegeben, wenn der aktuelle Sicherheitsdeskriptor das übergeordnete Element ist.

 

 
