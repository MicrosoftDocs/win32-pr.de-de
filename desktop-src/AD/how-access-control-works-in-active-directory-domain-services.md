---
title: Funktionsweise Access Control in Active Directory Domain Services
description: Die Zugriffssteuerung für Objekte in Active Directory Domain Services basiert auf Windows NT- und Windows 2000-Zugriffssteuerungsmodellen.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Sicherheit, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f53cdd7b958313b3cb16bc538addc73b42bd0dc917160176422b85c959c8c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188286"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Funktionsweise Access Control in Active Directory Domain Services

Die Zugriffssteuerung für Objekte in Active Directory Domain Services basiert auf Windows NT- und Windows 2000-Zugriffssteuerungsmodellen. Weitere Informationen und eine ausführliche Beschreibung dieses Modells und seiner Komponenten wie Sicherheitsdeskriptoren, Zugriffstoken, SIDs, ACLs und ACEs finden Sie unter Access Control [Model](/windows/desktop/SecAuthZ/access-control-model).

Zugriffsberechtigungen für Ressourcen in Active Directory Domain Services werden in der Regel mithilfe eines Zugriffssteuerungseintrags (ACE) gewährt. Ein ACE definiert eine Zugriffs- oder Überwachungsberechtigung für ein Objekt für einen bestimmten Benutzer oder eine bestimmte Gruppe. Eine Zugriffssteuerungsliste (Access Control List, ACL) ist die geordnete Auflistung von Zugriffssteuerungseinträgen, die für ein Objekt definiert sind. Ein Sicherheitsdeskriptor unterstützt Eigenschaften und Methoden zum Erstellen und Verwalten von ACLs. Weitere Informationen zu Sicherheitsmodellen finden Sie unter [Sicherheit](/windows/desktop/SecAuthZ/access-control) oder Windows *2000 Server Resource Kit*. (Diese Ressource ist in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.)

Die grundlegende Gliederung des Sicherheitsmodells ist:

-   Sicherheitsdeskriptor. Jedes Verzeichnisobjekt verfügt über einen eigenen Sicherheitsdeskriptor, der Sicherheitsdaten enthält, die das Objekt schützen. Der Sicherheitsdeskriptor kann eine DACL (Discretionary Access Control List) enthalten. Eine DACL enthält eine Liste von ACEs. Jeder ACE gewährt oder verweigert einem Benutzer oder einer Gruppe Zugriffsrechte. Die Zugriffsrechte entsprechen den Vorgängen, z. B. Lese- und Schreibeigenschaften, die für das Objekt ausgeführt werden können.
-   Sicherheitskontext. Wenn auf ein Verzeichnisobjekt zugegriffen wird, gibt die Anwendung die Anmeldeinformationen des Sicherheitsprinzipals an, der den Zugriff versucht. Bei der Authentifizierung bestimmen diese Anmeldeinformationen den Sicherheitskontext der Anwendung, einschließlich der Gruppenmitgliedschaften und Berechtigungen, die dem Sicherheitsprinzipal zugeordnet sind. Weitere Informationen zu Sicherheitskontexten finden Sie unter [Sicherheitskontexte und Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Zugriffsüberprüfung. Das System gewährt nur Dann Zugriff auf ein Objekt, wenn der Sicherheitsdeskriptor des Objekts dem Sicherheitsprinzipal, der den Vorgang versucht, die erforderlichen Zugriffsrechte gewährt (oder gruppen, zu denen der Sicherheitsprinzipal gehört).

In der folgenden Tabelle sind ADSI-Schnittstellen aufgeführt, die zum Bearbeiten der Zugriffssteuerungsfunktionen von Active Directory Domain Services.



| Schnittstelle                                                 | BESCHREIBUNG                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Wird zum Lesen und Schreiben von Sicherheitseigenschaften eines Verzeichnisdienstobjekts verwendet. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Wird zum Verwalten und Aufzählen aller ACEs für ein Verzeichnisdienstobjekt verwendet.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Wird zum Lesen und Schreiben von ACE-Eigenschaften verwendet.                                    |



 

 

 