---
description: Das Kerberos-Protokoll besteht aus drei unter Protokollen.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Kerberos-Unterprotokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216341"
---
# <a name="kerberos-subprotocols"></a>Kerberos-Unterprotokolle

Das [*Kerberos-Protokoll*](../secgloss/k-gly.md) besteht aus drei unter Protokollen.



| Unter Protokoll                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Authentifizierungsdienstaustausch](authentication-service-exchange.md)<br/>   | In diesem unter Protokoll gibt der [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) (KDC) dem Client einen Anmelde [*Sitzungsschlüssel*](../secgloss/s-gly.md) und ein Ticket-Zuteilungs Ticket (TGT).<br/> |
| [Ticket-Granting-Dienstaustausch](ticket-granting-service-exchange.md)<br/> | In diesem Subprotokoll verteilt der KDC einen Dienst Sitzungsschlüssel und ein Ticket für den Dienst.<br/>                                                                                                                                                                                                            |
| [Client-/Server-Exchange](client-server-exchange.md)<br/>                     | In diesem Subprotokoll stellt der Client das Ticket für den Zutritt zu einem Dienst dar.<br/>                                                                                                                                                                                                                         |



 

 

 
