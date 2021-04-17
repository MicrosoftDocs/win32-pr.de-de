---
title: Einschränkungen der gegenseitigen Authentifizierung mit Kerberos
description: Sowohl das Konto des Clients als auch das Konto des Diensts müssen sich in Domänen mit Windows 2000-oder gemischtem Modus befinden, da Kerberos-Dienste nicht in Domänen mit unterer Ebene verfügbar sind.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470860"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Einschränkungen der gegenseitigen Authentifizierung mit Kerberos

Sowohl das Konto des Clients als auch das Konto des Diensts müssen sich in Domänen mit Windows 2000-oder gemischtem Modus befinden, da Kerberos-Dienste nicht in Domänen mit unterer Ebene verfügbar sind. Außerdem müssen sich sowohl Client-als auch Dienst Konten in derselben Gesamtstruktur befinden, weil der Client-KDC den globalen Katalog verwendet, um nach dem Dienst Prinzipal Namen zu suchen.

Sowohl der Dienst als auch der Client müssen unter Windows 2000 ausgeführt werden. andernfalls schlägt die gegenseitige Authentifizierung mit Kerberos fehl, da frühere Versionen von Windows Kerberos nicht unterstützen.

Dienst Prinzipal Namen müssen den DNS-Namen des Host Servers enthalten, auf dem der Dienst ausgeführt wird. Sie müssen den DNS-Namen verwenden.

 

 




