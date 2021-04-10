---
title: Funktionsweise von Access Control in Active Directory Domain Services
description: Die Zugriffs Steuerung für Objekte in Active Directory Domain Services basiert auf Windows NT-und Windows 2000-Access-Control-Modellen.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Sicherheit, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948565"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Funktionsweise von Access Control in Active Directory Domain Services

Die Zugriffs Steuerung für Objekte in Active Directory Domain Services basiert auf Windows NT-und Windows 2000-Access-Control-Modellen. Weitere Informationen und eine ausführliche Beschreibung dieses Modells und seiner Komponenten, z. b. Sicherheits Deskriptoren, Zugriffs Token, SIDs, ACLs und ACEs, finden Sie unter [Access Control Modell](/windows/desktop/SecAuthZ/access-control-model).

Zugriffsberechtigungen für Ressourcen in Active Directory Domain Services werden in der Regel durch die Verwendung eines Zugriffs Steuerungs Eintrags (Access Control Entry, ACE) gewährt. Ein ACE definiert eine Zugriffs-oder Audit-Berechtigung für ein Objekt für einen bestimmten Benutzer oder eine bestimmte Gruppe. Eine Zugriffs Steuerungs Liste (Access Control List, ACL) ist die geordnete Auflistung von Zugriffs Steuerungs Einträgen, die für ein Objekt definiert sind. Eine Sicherheits Beschreibung unterstützt Eigenschaften und Methoden, mit denen ACLs erstellt und verwaltet werden. Weitere Informationen zu Sicherheitsmodellen finden Sie unter [Security](/windows/desktop/SecAuthZ/access-control) oder The *Windows 2000 Server Resource Kit*. (Diese Ressource ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.)

Der grundlegende Umriss des Sicherheitsmodells lautet wie folgt:

-   Sicherheits Beschreibung. Jedes Verzeichnis Objekt verfügt über eine eigene Sicherheits Beschreibung, die Sicherheitsdaten enthält, mit denen das Objekt geschützt wird. Die Sicherheits Beschreibung kann eine freigegebene Zugriffs Steuerungs Liste (DACL) enthalten. Eine DACL enthält eine Liste von ACEs. Jeder ACE gewährt oder verweigert einem Benutzer oder einer Gruppe Zugriffsrechte. Die Zugriffsrechte entsprechen den Vorgängen, z. b. dem Lesen und Schreiben von Eigenschaften, die für das Objekt ausgeführt werden können.
-   Sicherheitskontext. Wenn auf ein Verzeichnis Objekt zugegriffen wird, gibt die Anwendung die Anmelde Informationen des Sicherheits Prinzipals an, der den Zugriffs Versuch durchführen soll. Bei der Authentifizierung bestimmen diese Anmelde Informationen den Sicherheitskontext der Anwendung, der die Gruppenmitgliedschaften und Berechtigungen enthält, die dem Sicherheits Prinzipal zugeordnet sind. Weitere Informationen zu Sicherheits Kontexten finden Sie unter [Sicherheits Kontexte und Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Zugriffs Überprüfung. Das System gewährt nur dann Zugriff auf ein Objekt, wenn die Sicherheits Beschreibung des Objekts die erforderlichen Zugriffsrechte für den Sicherheits Prinzipal erteilt, der den Vorgang versucht (oder für Gruppen, zu denen der Sicherheits Prinzipal gehört).

In der folgenden Tabelle sind die ADSI-Schnittstellen aufgeführt, mit denen die Zugriffs Steuerungsfunktionen von Active Directory Domain Services bearbeitet werden.



| Schnittstelle                                                 | BESCHREIBUNG                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Wird verwendet, um Sicherheitseigenschaften eines Verzeichnisdienst Objekts zu lesen und zu schreiben. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Wird verwendet, um alle ACEs für ein Verzeichnisdienst Objekt zu verwalten und aufzuzählen.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Dient zum Lesen und Schreiben von ACE-Eigenschaften.                                    |



 

 

 