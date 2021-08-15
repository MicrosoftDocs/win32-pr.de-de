---
title: Suchen eines Anwendungsverzeichnispartitionshostservers
description: In diesem Thema wird beschrieben, wie Sie einen Hostserver für die Anwendungsverzeichnispartition suchen.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Suchen eines Anwendungsverzeichnispartitionshostservers AD
- Anwendungsverzeichnispartitionen AD , Suchen eines Hostservers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186791"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Suchen eines Anwendungsverzeichnispartitionshostservers

Der NetLogon-Dienst registriert die folgende Liste von SRV-Einträgen für eine Anwendungsverzeichnispartition:

-   \_ldap. \_ Tcp.<partition name>
-   \_ldap. \_ tcp. <site name> . \_ Websites.<partition name>

Um einen Domänencontroller zu finden, der ein Replikat einer angegebenen Anwendungsverzeichnispartition hostet, rufen Sie die [**DsGetDcName-Funktion**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) auf, wobei der *DomainName-Parameter* auf den DNS-Namen der Anwendungsverzeichnispartition und das **Flag DS \_ ONLY LDAP \_ \_ NEEDED** im *Flags-Parameter* festgelegt ist. Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie mithilfe der **DsGetDcName-Funktion** einen Domänencontroller finden, der ein Replikat einer Anwendungsverzeichnispartition hostet, finden Sie unter [Beispielcode zum Suchen eines Hostservers für die Anwendungsverzeichnispartition.](example-code-for-locating-an-application-directory-partition-host-server.md)

 

 




