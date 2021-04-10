---
title: Gruppen auf Mitglieds Servern und Windows 2000 Professional
description: Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, gibt es eine lokale Sicherheitsdatenbank.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Gruppen auf Mitglieds Servern und Windows 2000 Professional AD
- Gruppen Ad, Gruppen auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309283"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Gruppen auf Mitglieds Servern und Windows 2000 Professional

Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, gibt es eine lokale Sicherheitsdatenbank. Diese lokale Sicherheitsdatenbank kann eigene lokale Benutzer-und lokale Gruppen enthalten, deren Bereich nur dem Computer entspricht, auf dem Sie erstellt werden. Verwenden Sie den WinNT-Anbieter, wenn Sie diese Arten von Benutzern und Gruppen auf Mitglieds Servern und Computern verwalten, die auf Windows NT-Arbeitsstationen oder Windows 2000 Professional ausgeführt werden.

Wenn ein Mitglieds Server oder ein Computer, auf dem Windows 2000 Professional oder Windows 2000 Professional ausgeführt wird, Mitglied einer Windows 2000-Domäne ist, können die Gruppen oder Benutzer in der Domäne in der lokalen Sicherheitsdatenbank verwendet werden, um der Gruppe auf dem betreffenden Computer Rechte zuzuweisen.

Verwenden Sie beim Verwalten von Gruppen in einer Windows 2000-Domäne mithilfe von ADSI den LDAP-Anbieter. Verwenden Sie den WinNT-Anbieter, wenn Sie Gruppen auf Mitglieds Servern und Computern verwalten, die auf der Windows NT-Arbeitsstation oder Windows 2000 Professional ausgeführt werden.

Sie müssen mindestens eine Instanz an jeden Anbieter binden: 1) binden Sie an den LDAP-Anbieter, um den ADsPath für die Gruppe oder den Benutzer abzurufen, die Sie einer Gruppe in der lokalen Datenbank hinzufügen möchten, und 2) binden an den WinNT-Anbieter, um diesen Benutzer bzw. diese Gruppe zu einer lokalen Gruppe hinzuzufügen.

 

 




