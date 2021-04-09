---
title: Benutzer in Active Directory Domain Services
description: Active Directory Domain Services enthält einen Verzeichnisdienst, in dem Domänen-, Benutzer-, Benutzergruppen-und Sicherheitsdaten gespeichert werden.
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Benutzer in Active Directory Domain Services Active Directory
- Benutzer, Active Directory-Domänen Dienste
- Active Directory-Domänen Dienste, Benutzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038725"
---
# <a name="users-in-active-directory-domain-services"></a>Benutzer in Active Directory Domain Services

Active Directory Domain Services enthält einen Verzeichnisdienst, in dem Domänen-, Benutzer-, Benutzergruppen-und Sicherheitsdaten gespeichert werden.

Unter Windows NT 4,0 und früher können Sie Funktionen wie z. b. " [**nettuseradd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd)", " [**nettuserenum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum)", " [**nettuserdel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel)" usw. zum Verwalten von Benutzern, Benutzergruppen und anderen Netzwerkelementen verwenden. Unter Windows 2000 und neueren Versionen von Windows bietet ADSI einheitlichen und sicheren Zugriff auf diese Elemente und deren Eigenschaften. Beachten Sie, dass ADSI einen Windows NT 4,0-Anbieter bietet, der es Ihnen ermöglicht, mithilfe von ADSI Benutzer, Benutzergruppen und Computer auf Windows NT 4,0-Systemen zu verwalten. Es gibt auch Anbieter für Windows Server 2008 Enterprise (Server Core-Installation), Microsoft Exchange 5,5, Microsoft Internet Information Server (IIS), Novell NetWare-Verzeichnisdienste (NDS) und Novell NetWare 3. Das heißt, es ist ein einzelner Satz standardisierter Methoden zum Verwalten von Benutzern und Benutzergruppen für Windows NT, NDS und NetWare 3.

Außerdem ist Windows 2000 ein multimasterverzeichnis. Das heißt, Änderungen an Benutzern, Benutzergruppen und anderen Daten, die im Verzeichnis gespeichert werden, können auf jedem beliebigen Domänen Controller vorgenommen werden. Unter Windows 2000 müssen Sie den primären Domänen Controller (PDC) nicht finden und Änderungen an Benutzer-und Benutzergruppen auf dem PDC vornehmen.

Windows 2000 führt außerdem einen neuen hierarchischen Namespace in einer Domäne ein, die als Organisationseinheit (OU) bezeichnet wird. Eine Organisationseinheit kann Computer, Benutzer, Benutzergruppen und andere Netzwerk Objekte enthalten. In der Regel wird eine Organisationseinheit für die Gruppierung von Elementen zu Verwaltungszwecken verwendet, z. b. die Delegierung von Administratorrechten und das Zuweisen von Richtlinien zur Gruppe als eine Einheit.

Domänen, Organisationseinheiten, Benutzer, Benutzergruppen, Computer und andere Netzwerkelemente werden in Active Directory Domain Services als Objekte gespeichert. In Windows 2000 und neueren Versionen von Windows fügen Sie Benutzer, Benutzergruppen und Computer weiterhin einer Domäne hinzu. Sie haben jedoch die Möglichkeit, diese Objekte einem OE-Container oder einem anderen Containertyp hinzuzufügen, den das Objekt, das Sie hinzufügen möchten, im **Besitz** Ende Attribut des **classSchema** -Objekts definiert. Dabei handelt es sich um ein Attribut für das **classSchema** -Objekt eines Objekts, und dieses Attribut schränkt die Typen von Objekten ein, die dieses Objekt enthalten können.

 

 