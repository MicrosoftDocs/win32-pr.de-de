---
title: Herstellen einer Verbindung mit Active Directory
description: Für den Zugriff auf Active Directory werden mehrere Methoden verwendet.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Herstellen einer Verbindung mit Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947353"
---
# <a name="connecting-to-active-directory"></a>Herstellen einer Verbindung mit Active Directory

Für den Zugriff auf Active Directory werden mehrere Methoden verwendet. Es wird empfohlen, dass Sie die ADSI-API verwenden, um auf Active Directory zuzugreifen. ADSI implementiert das LDAP-Protokoll für die Kommunikation mit Active Directory. In den folgenden Codebeispielen wird gezeigt, wie Sie auf Active Directory zugreifen können.


```VB
Set ns = GetObject("LDAP:")
```



Dadurch wird der LDAP-Anbieter geöffnet und zum Abrufen von Daten vorbereitet. Es wird keine Verbindung hergestellt, bis Daten angefordert werden. Wenn Daten angefordert werden, versucht ADSI mithilfe des Serverlocatorpunkt-Dienstanbieter, den besten Domänen Controller (DC) für die Verbindung zu finden und stellt eine Verbindung mit dem Server her. Dieser Prozess wird als Server lose Bindung bezeichnet.

Mit ADSI können Sie auch den Servernamen angeben, der für die Verbindung verwendet werden soll.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



In einem anderen Szenario kennen Sie möglicherweise nur den Domänen Namen, jedoch nicht den Namen des jeweiligen Servers. Auch hier können Sie mit ADSI den Domänen Namen angeben. In Windows 2000 wird der Domänen Name als DNS-Name dargestellt. Wenn beispielsweise Joe de, der Netzwerkadministrator, eine Verbindung mit dem Domänen Namen herstellt, könnte er das folgende Codebeispiel verwenden.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI stellt eine Verbindung mit einem der Domänen Controller in der Fabrikam.com-Domäne her.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binden an Active Directory Objekte](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




