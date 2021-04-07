---
title: Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
description: In diesem Thema wird gezeigt, wie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, aufgelistet werden.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional AD
- Benutzer AD, Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
- Active Directory, verwenden von Benutzern, Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724552"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Auflisten von Benutzern auf Mitglieds Servern und Windows 2000 Professional

In diesem Thema wird gezeigt, wie alle Benutzer in einer lokalen Sicherheitsdatenbank auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, aufgelistet werden.

**So zählen Sie die Benutzer auf**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto, das über ausreichende Rechte für den Zugriff auf den Computer verfügt.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ". Der &lt; Parameter "Computername &gt; " ist der Name des Computers, auf dessen Gruppen zugegriffen werden soll. Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem WinNT-Anbieter Parser, einige mehrdeutigkeits Auflösungs Abfragen zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.
    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.
2.  Fügen Sie "User" der Eigenschaft " [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) " hinzu. Dies bewirkt, dass die Enumeration nur Objekte enthält, die über die Objektklasse "User" verfügen.
3.  Listet die Objekte auf. Verwenden Sie für jedes Benutzerobjekt die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -oder [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) -Schnittstellen Methoden, um die Benutzereigenschaften zu lesen.

 

 