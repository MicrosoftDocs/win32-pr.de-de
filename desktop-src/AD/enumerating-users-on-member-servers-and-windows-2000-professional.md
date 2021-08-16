---
title: Aufzählen von Benutzern auf Mitgliedsservern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie Sie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitgliedsservern und Computern aufzählen, die auf Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Aufzählen von Benutzern auf Mitgliedsservern und Windows 2000 Professional AD
- users AD , Enumerating Users on Member Servers and Windows 2000 Professional
- Active Directory, Using, Users, Enumerating Users on Member Servers and Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694877"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Aufzählen von Benutzern auf Mitgliedsservern und Windows 2000 Professional

In diesem Thema wird gezeigt, wie Sie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitgliedsservern und Computern aufzählen, die auf Windows 2000 Professional.

**So enumerieren Sie die Benutzer**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf diesen Computer verfügt.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat unter Verwendung des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI anweisen zu können, dass es an einen Computer WinNT:// <computer name> <computer> , ". Der Parameter &lt; "Computername" &gt; ist der Name des Computers, auf den die Gruppen zugreifen sollen. Dieser Parameter weist ADSI an, an einen Computer zu binden, und ermöglicht es dem WinNT-Anbieterparser, einige Abfragen zur Mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie binden.
    3.  Binden sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Fügen Sie der [**IADsContainer.Filter-Eigenschaft "user"**](/windows/desktop/ADSI/iadscontainer-property-methods) hinzu. Dies bewirkt, dass die Enumeration nur Objekte enthält, die über die Objektklasse "user" verfügen.
3.  Enumerieren Sie die -Objekte. Verwenden Sie für jedes Benutzerobjekt die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) oder [**IADsUser-Schnittstellenmethoden,**](/windows/desktop/api/iads/nn-iads-iadsuser) um die Benutzereigenschaften zu lesen.

 

 