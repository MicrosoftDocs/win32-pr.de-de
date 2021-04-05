---
title: Suchen eines Anwendungsverzeichnis-Partitions Host Servers
description: In diesem Thema wird beschrieben, wie Sie einen Anwendungsverzeichnis-Partitions Host Server finden.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Suchen eines Anwendungsverzeichnis-Partitions Host Server-AD
- Anwendungsverzeichnis Partitionen AD, Suchen eines Host Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707607"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Suchen eines Anwendungsverzeichnis-Partitions Host Servers

Der Anmeldedienst registriert die folgende Liste der SRV-Einträge für eine Anwendungsverzeichnis Partition:

-   \_LDAP. \_ TCP.<partition name>
-   \_LDAP. \_ TCP. <site name> . \_ Websites.<partition name>

Wenn Sie einen Domänen Controller suchen möchten, der ein Replikat einer angegebenen Anwendungsverzeichnis Partition hostet, müssen Sie die Funktion [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) mit dem Parameter *Domain Name* auf den DNS-Namen der Anwendungsverzeichnis Partition und das nur für die **nur erforderliche DS-Flag für \_ \_ LDAP \_ erforderliche** Flag im *Flags* -Parameter festlegen. Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie mithilfe der **DsGetDcName** -Funktion einen Domänen Controller suchen, der ein Replikat einer Anwendungsverzeichnis Partition hostet, finden Sie unter [Beispielcode für die Suche eines Anwendungsverzeichnis-Partitions Host Servers](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




