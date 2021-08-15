---
title: Verwenden eines lokalen Benutzerkontos als Dienstanmeldungskonto
description: Ein lokales Benutzerkonto (Namensformat \ 0034;. \\ UserName \ 0034;) ist nur in der SAM-Datenbank des Hostcomputers vorhanden. Sie verfügt nicht über ein Benutzerobjekt in Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186855"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Verwenden eines lokalen Benutzerkontos als Dienstanmeldungskonto

Ein lokales Benutzerkonto (Namensformat: ". \\ *UserName*") ist nur in der SAM-Datenbank des Hostcomputers vorhanden. Sie verfügt nicht über ein Benutzerobjekt in Active Directory Domain Services. Dies bedeutet, dass ein lokales Konto nicht von der Domäne authentifiziert werden kann. Folglich hat ein Dienst, der im Sicherheitskontext eines lokalen Benutzerkontos ausgeführt wird, keinen Zugriff auf Netzwerkressourcen (außer als anonymer Benutzer) und kann keine gegenseitige Kerberos-Authentifizierung unterstützen, bei der der Dienst von seinen Clients authentifiziert wird. Aus diesen Gründen eignen sich lokale Benutzerkonten normalerweise nicht für verzeichnisfähige Dienste. Auf der Plusseite können Fehler im Dienst das System nicht beschädigen. Wenn Ihr Dienst unter diesen Einschränkungen ausgeführt werden kann, sollte er ausgeführt werden.

 

 




