---
title: Verwenden eines lokalen Benutzerkontos als Dienst Anmelde Konto
description: Ein lokales Benutzerkonto (Namensformat \ 0034;. \\ Benutzername \ 0034;) ist nur in der SAM-Datenbank des Host Computers vorhanden. in Active Directory Domain Services ist kein Benutzerobjekt vorhanden.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100594"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Verwenden eines lokalen Benutzerkontos als Dienst Anmelde Konto

Ein lokales Benutzerkonto (Namensformat: "). \\ Der *Benutzername*") ist nur in der SAM-Datenbank des Host Computers vorhanden. in Active Directory Domain Services ist kein Benutzerobjekt vorhanden. Dies bedeutet, dass ein lokales Konto nicht von der Domäne authentifiziert werden kann. Folglich hat ein Dienst, der im Sicherheitskontext eines lokalen Benutzerkontos ausgeführt wird, keinen Zugriff auf Netzwerkressourcen (mit Ausnahme eines anonymen Benutzers) und kann keine gegenseitige Kerberos-Authentifizierung unterstützen, bei der der Dienst von seinen Clients authentifiziert wird. Aus diesen Gründen eignen sich lokale Benutzerkonten normalerweise nicht für verzeichnisfähige Dienste. Auf der Plus Seite können Fehler im Dienst das System nicht beschädigen. Wenn Ihr Dienst unter diesen Beschränkungen ausgeführt werden kann, sollte dies der Fall sein.

 

 




