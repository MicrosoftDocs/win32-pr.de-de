---
title: Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema werden die Schritte beschrieben, die zum Erstellen eines Benutzers auf einem Mitglieds Server oder einem Computer mit Windows 2000 Professional verwendet werden.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
- Benutzer AD, Erstellen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Erstellen eines Benutzers auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038778"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Erstellen von Benutzern auf Mitglieds Servern und Windows 2000 Professional

**So erstellen Sie einen Benutzer**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf den Computer verfügt.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI mitzuteilen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ". Der Computer &lt; Name &gt; ist der Name des Computers, auf dessen Gruppen Sie zugreifen möchten. Mit diesem Parameter wird ADSI mitgeteilt, dass es an einen Computer gebunden ist. der Parser des WinNT-Anbieters kann einige mehrdeutigkeits Auflösungs Abfragen überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.
    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.
2.  Geben Sie "User" als Klasse an, indem Sie [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um den Benutzer hinzuzufügen.
3.  Schreiben Sie den Benutzer mithilfe von " [**IADs. * tinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)" in die Sicherheitsdatenbank des Computers.

 

 