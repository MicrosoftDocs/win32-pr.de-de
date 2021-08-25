---
description: Das Kerberos-Protokoll besteht aus drei Unterprotokollen.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Kerberos-Unterprotokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ea1ababaf1ec7fe4e80112d4c1f69dc8bfc242a40cea56675d08198188a130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013360"
---
# <a name="kerberos-subprotocols"></a>Kerberos-Unterprotokollen

Das [*Kerberos-Protokoll*](../secgloss/k-gly.md) besteht aus drei Unterprotokollen.



| Unterprotokoll                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Authentifizierungsdienstaustausch](authentication-service-exchange.md)<br/>   | In diesem Unterprotokoll erhält der [*clientseitige Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) einen [*Anmeldesitzungsschlüssel*](../secgloss/s-gly.md) und ein Ticket-Granting Ticket (TGT).<br/> |
| [Ticket-Granting-Dienstaustausch](ticket-granting-service-exchange.md)<br/> | In diesem Unterprotokoll verteilt das KDC einen Dienstsitzungsschlüssel und ein Ticket für den Dienst.<br/>                                                                                                                                                                                                            |
| [Client-/Server-Exchange](client-server-exchange.md)<br/>                     | In diesem Unterprotokoll stellt der Client das Ticket für den Zugang zu einem Dienst vor.<br/>                                                                                                                                                                                                                         |



 

 

 
