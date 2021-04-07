---
title: Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie ein Benutzer von einem Mitglieds Server oder Computer, der unter Windows 2000 Professional ausgeführt wird, gelöscht wird.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- Benutzer AD, Löschen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
- Löschen eines Benutzers
- Server, Löschen eines Benutzers
- Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038770"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Löschen von Benutzern auf Mitglieds Servern und Windows 2000 Professional

In diesem Thema wird gezeigt, wie ein Benutzer von einem Mitglieds Server oder Computer, der unter Windows 2000 Professional ausgeführt wird, gelöscht wird.

**So löschen Sie einen Benutzer**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI mitzuteilen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ". Der &lt; Parameter "Computername &gt; " ist der Name des Computers, auf dessen Gruppen Sie zugreifen möchten. Dieser Parameter benachrichtigt ADSI, dass er an einen Computer gebunden ist, und ermöglicht es dem WinNT-Anbieter Parser, einige mehrdeutigkeits Auflösungs Abfragen zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.
    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.
2.  Geben Sie "User" mithilfe von " [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) " als Klasse an, um den Benutzer zu löschen.

    Beachten Sie, dass Sie [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) nicht zum Commit der Änderung an den Container anrufen müssen. Der [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) -Befehl führt einen Commit für das Löschen des Benutzers direkt zum Verzeichnis aus.

 

 