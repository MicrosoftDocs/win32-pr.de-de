---
description: Eine Zugriffssteuerungsliste (Access Control List, ACL) ist eine Liste von Zugriffssteuerungseinträgen (Access Control Entries, ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Zugriffssteuerungslisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a788f02f8a04711be7db8268833375b2519d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348940"
---
# <a name="access-control-lists"></a>Zugriffssteuerungslisten

Eine [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) ist eine Liste von [Zugriffs Steuerungs Einträgen (Access Control Entries](access-control-entries.md) , ACE). Jeder ACE in einer ACL bezeichnet einen [Vertrauensnehmer](trustees.md) und gibt die [Zugriffsrechte](access-rights-and-access-masks.md) an, die dem Vertrauensnehmer gewährt, verweigert oder im Hinblick auf den Vertrauensnehmer überwacht werden. Die [Sicherheits Beschreibung](security-descriptors.md) für ein Sicherungs [fähiges Objekt](securable-objects.md) kann zwei Arten von ACLs enthalten: eine DACL und eine SACL.

Eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) identifiziert die Vertrauens nehmer, denen der Zugriff auf ein Sicherungs fähiges Objekt gestattet oder verweigert wird. Wenn ein [*Prozess*](/windows/desktop/SecGloss/p-gly) versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, prüft das System die ACEs in der DACL des Objekts, um zu bestimmen, ob Ihnen Zugriff gewährt werden soll. Wenn das Objekt keine DACL hat, gewährt das System vollen Zugriff auf alle. Wenn die DACL des Objekts keine ACEs hat, verweigert das System alle Zugriffsversuche auf das Objekt, da die DACL keine Zugriffsrechte zulässt. Das System überprüft die ACEs nacheinander, bis ein oder mehrere ACEs gefunden werden, die alle angeforderten Zugriffsrechte zulassen, oder bis eine der angeforderten Zugriffsrechte verweigert wird. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md). Informationen dazu, wie Sie eine DACL ordnungsgemäß erstellen, finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).

Eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) ermöglicht Administratoren das Protokollieren von Zugriffsversuchen auf ein gesichertes Objekt. Jeder ACE gibt die Arten von Zugriffsversuchen durch einen angegebenen Vertrauens nehmer an, die bewirken, dass das System einen Datensatz im Sicherheits Ereignisprotokoll generiert. Ein ACE in einer SACL kann Überwachungsdaten Sätze generieren, wenn ein Zugriffs Versuch fehlschlägt, wenn er erfolgreich ist oder beides. Weitere Informationen zu SACLs finden Sie unter [Audit Generation](audit-generation.md) and [SACL Access Right](sacl-access-right.md).

Versuchen Sie nicht, direkt mit dem Inhalt einer ACL zu arbeiten. Um sicherzustellen, dass ACLs semantisch korrekt sind, verwenden Sie die entsprechenden Funktionen zum Erstellen und Bearbeiten von ACLs. Weitere Informationen finden Sie unter [erhalten von Informationen aus einer ACL](getting-information-from-an-acl.md) und [erstellen oder Ändern einer ACL](creating-or-modifying-an-acl.md).

ACLs ermöglichen auch die Zugriffs Steuerung für Microsoft Active Directory Directory-Dienst Objekte. Active Directory Service Interfaces (ADSI) beinhalten Routinen zum Erstellen und Ändern des Inhalts dieser ACLs. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf Active Directory Objekte](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services).

 

 
