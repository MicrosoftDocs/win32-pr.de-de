---
title: Erstellen von Benutzern auf Mitgliedsservern und Windows 2000 Professional
description: In diesem Thema werden die Schritte zum Erstellen eines Benutzers auf einem Mitgliedsserver oder Computer mit Windows 2000 Professional beschrieben.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Erstellen von Benutzern auf Mitgliedsservern und Windows 2000 Professional AD
- Benutzer AD , erstellen einen Benutzer auf Mitgliedsservern und Windows 2000 Professional
- Active Directory, using, users, creating a user on member servers and Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21490302b025e20f836cbbc957d0f86824b3456d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881577"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Erstellen von Benutzern auf Mitgliedsservern und Windows 2000 Professional

**So erstellen Sie einen Benutzer**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf diesen Computer verfügt.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat mithilfe des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI mitzuteilen, dass die Bindung an einen Computer erfolgt: "WinNT:// <computer name> , &lt; &gt; Computer". Der &lt; &gt; Computername "Computername" ist der Name des Computers, auf dessen Gruppen Sie zugreifen möchten. Dieser Parameter teilt ADSI mit, dass er an einen Computer gebunden ist, und ermöglicht es dem Parser des WinNT-Anbieters, einige Mehrdeutigkeitsauflösungsabfragen zu überspringen, um zu bestimmen, an welchen Objekttyp Sie binden.
    3.  Binden Sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Geben Sie "user" als Klasse an, indem [**Sie IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um den Benutzer hinzuzufügen.
3.  Schreiben Sie den Benutzer mithilfe von [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)in die Sicherheitsdatenbank des Computers.

 

 
