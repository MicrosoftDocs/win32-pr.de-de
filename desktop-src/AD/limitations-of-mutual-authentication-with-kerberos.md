---
title: Einschränkungen der gegenseitigen Authentifizierung mit Kerberos
description: Sowohl das Clientkonto als auch das Dienstkonto müssen sich in Windows 2000-Domänen im nativ oder gemischten Modus befinden, da Kerberos-Dienste in Downleveldomänen nicht verfügbar sind.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bdc2f8cfe87d3cece32987ee0958000b1186775257013ce27f5950c6ac8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187064"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Einschränkungen der gegenseitigen Authentifizierung mit Kerberos

Sowohl das Clientkonto als auch das Dienstkonto müssen sich in Windows 2000-Domänen im nativ oder gemischten Modus befinden, da Kerberos-Dienste in Downleveldomänen nicht verfügbar sind. Darüber hinaus müssen sich sowohl Client- als auch Dienstkonten in derselben Gesamtstruktur enthalten, da das KDC des Clients den globalen Katalog verwendet, um nach dem Dienstprinzipalnamen zu suchen.

Sowohl der Dienst als auch der Client müssen auf Windows 2000 ausgeführt werden. Andernfalls kann die gegenseitige Authentifizierung mit Kerberos nicht ausgeführt werden, da frühere Versionen von Windows Kerberos nicht unterstützen.

Dienstprinzipalnamen müssen den DNS-Namen des Hostservers enthalten, auf dem der Dienst ausgeführt wird. Sie müssen den DNS-Namen verwenden.

 

 




