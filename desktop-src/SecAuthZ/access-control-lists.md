---
description: Eine Zugriffssteuerungsliste (Access Control List, ACL) ist eine Liste von Zugriffssteuerungseinträgen (Access Control Entries, ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Zugriffssteuerungslisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7021767830dead84f2ea965c46ca205257a2f18443f352ec85becc0139e30e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785660"
---
# <a name="access-control-lists"></a>Zugriffssteuerungslisten

Eine [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) (Access Control List, ACL) ist eine Liste von [Zugriffssteuerungseinträgen](access-control-entries.md) (ACE). Jeder ACE in einer ACL bezeichnet einen [Vertrauensnehmer](trustees.md) und gibt die [Zugriffsrechte](access-rights-and-access-masks.md) an, die dem Vertrauensnehmer gewährt, verweigert oder im Hinblick auf den Vertrauensnehmer überwacht werden. Der [Sicherheitsdeskriptor für](security-descriptors.md) ein [sicherungsfähiges](securable-objects.md) Objekt kann zwei Arten von ACLs enthalten: eine DACL und eine SACL.

Eine [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) identifiziert die Vertrauenshänder, denen der Zugriff auf ein sicherungsfähiges Objekt gestattet oder verweigert wird. Wenn ein [*Prozess*](/windows/desktop/SecGloss/p-gly) versucht, auf ein sicherungsfähiges Objekt zu zugreifen, überprüft das System die ACEs in der DACL des Objekts, um zu bestimmen, ob der Zugriff darauf gewährt werden soll. Wenn das Objekt nicht über eine DACL verfügt, gewährt das System allen Vollzugriff. Wenn die DACL des Objekts über keine ACEs verfügt, verweigert das System alle Zugriffsversuche auf das Objekt, da die DACL keine Zugriffsrechte zulädt. Das System überprüft die ACEs nacheinander, bis ein oder mehrere ACEs gefunden werden, die alle angeforderten Zugriffsrechte zulassen, oder bis eines der angeforderten Zugriffsrechte verweigert wird. Weitere Informationen finden Sie unter Steuern des Zugriffs auf ein [Objekt durch DACLs.](how-dacls-control-access-to-an-object.md) Informationen zum ordnungsgemäßen Erstellen einer DACL finden Sie unter [Erstellen einer DACL.](/windows/desktop/SecBP/creating-a-dacl)

Eine [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) ermöglicht Administratoren das Protokollieren von Zugriffsversuchen auf ein gesichertes Objekt. Jeder ACE gibt die Zugriffsversuche eines angegebenen Vertrauenshänders an, die dazu führen, dass das System einen Datensatz im Sicherheitsereignisprotokoll generiert. Ein ACE in einer SACL kann Überwachungsdatensätze generieren, wenn ein Zugriffsversuch fehlschlägt, wenn er erfolgreich ist, oder beides. Weitere Informationen zu SACLs finden Sie unter [Audit Generation](audit-generation.md) and [SACL Access Right](sacl-access-right.md).

Versuchen Sie nicht, direkt mit dem Inhalt einer ACL zu arbeiten. Um sicherzustellen, dass ACLs semantisch korrekt sind, verwenden Sie die entsprechenden Funktionen, um ACLs zu erstellen und zu bearbeiten. Weitere Informationen finden Sie unter [Abrufen von Informationen aus einer ACL](getting-information-from-an-acl.md) und Erstellen oder Ändern einer [ACL.](creating-or-modifying-an-acl.md)

ACLs ermöglichen auch die Zugriffssteuerung für Microsoft Active Directory-Verzeichnisdienstobjekte. Active Directory-Dienstschnittstellen (ADSI) enthalten Routinen zum Erstellen und Ändern des Inhalts dieser ACLs. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf Active Directory-Objekte.](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services)

 

 
