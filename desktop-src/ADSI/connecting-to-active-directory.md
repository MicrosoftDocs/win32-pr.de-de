---
title: Herstellen einer Verbindung mit Active Directory
description: Es gibt mehrere Methoden, die für den Zugriff auf Active Directory verwendet werden.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Herstellen einer Verbindung mit Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6afd5aa0edd8a4c4a87bae7cde6a135fc3467771eed2dbc0cb7673984040832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692008"
---
# <a name="connecting-to-active-directory"></a>Herstellen einer Verbindung mit Active Directory

Es gibt mehrere Methoden, die für den Zugriff auf Active Directory verwendet werden. Es wird empfohlen, die ADSI-API für den Zugriff auf Active Directory zu verwenden. ADSI implementiert das LDAP-Protokoll für die Kommunikation mit Active Directory. In den folgenden Codebeispielen wird der Zugriff auf Active Directory gezeigt.


```VB
Set ns = GetObject("LDAP:")
```



Dadurch wird der LDAP-Anbieter geöffnet und zum Abrufen von Daten vorbereitet. Es wird keine Verbindung hergestellt, bis Daten angefordert werden. Wenn Daten angefordert werden, versucht ADSI mithilfe des Locatordiensts, den besten Domänencontroller (DC) für die Verbindung zu finden und eine Verbindung mit dem Server herzustellen. Dieser Prozess wird als serverlose Bindung bezeichnet.

MIT ADSI können Sie auch den Servernamen angeben, der für die Verbindung verwendet werden soll.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



In einem anderen Szenario kennen Sie möglicherweise nur den Domänennamen, aber nicht den spezifischen Servernamen. Auch hier können Sie mit ADSI den Domänennamen angeben. In Windows 2000 wird der Domänenname als DNS-Name dargestellt. Wenn sich beispielsweise Joe Worden, der Netzwerkadministrator, für die Verbindung mithilfe des Domänennamens entscheidet, könnte er das folgende Codebeispiel verwenden.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI wird eine Verbindung mit einem der Domänencontroller in der fabrikam.com herstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binden an Active Directory-Objekte](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




