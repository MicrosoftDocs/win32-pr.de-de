---
title: Löschen von Benutzern auf Mitgliedsservern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie Sie einen Benutzer von einem Mitgliedsserver oder Computer löschen, der auf Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- benutzer AD , löscht einen Benutzer auf Mitgliedsservern und Windows 2000 Professional
- Active Directory mit , Benutzern, Löschen von Benutzern auf Mitgliedsservern und Windows 2000 Professional
- Löschen eines Benutzers
- Server, Löschen eines Benutzers
- Löschen von Benutzern auf Mitgliedsservern und Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d457ad69b3bd83f6295bda262896e85e43ad35280038cbe879ebd5aaf187a47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019547"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Löschen von Benutzern auf Mitgliedsservern und Windows 2000 Professional

In diesem Thema wird gezeigt, wie Sie einen Benutzer von einem Mitgliedsserver oder Computer löschen, der auf Windows 2000 Professional.

**So löschen Sie einen Benutzer**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat unter Verwendung des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI zu informieren, dass es an einen Computer WinNT:// <computer name> <computer> , ". Der Parameter &lt; "Computername" &gt; ist der Name des Computers, auf den Sie zugreifen möchten. Dieser Parameter benachrichtigt ADSI, dass er an einen Computer bindunget, und ermöglicht es dem WinNT-Anbieterparser, einige Abfragen zur Auflösung von Mehrdeutigkeiten zu überspringen, um zu bestimmen, an welchen Objekttyp Sie binden.
    3.  Binden sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Geben Sie "user" als Klasse an, indem [**Sie IADsContainer.Delete verwenden,**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) um den Benutzer zu löschen.

    Beachten Sie, dass Sie [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) nicht aufrufen müssen, um die Änderung an den Container zu commiten. Der [**IADsContainer.Delete-Aufruf**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) überträgt das Löschen des Benutzers direkt im Verzeichnis.

 

 