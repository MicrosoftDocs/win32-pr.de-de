---
description: Sowohl C++-Anbieter als auch Client Anwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Sichern von C++-Clients und-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347320"
---
# <a name="securing-c-clients-and-providers"></a>Sichern von C++-Clients und-Anbietern

Sowohl C++-Anbieter als auch Client Anwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.

Client Anwendungen müssen den [DCOM-](setting-the-default-process-security-level-using-c-.md) Identitätswechsel und die [Authentifizierungs](setting-authentication-in-wmi.md) Ebenen beim Herstellen einer Verbindung mit WMI ordnungsgemäß festlegen. [Rückrufe von asynchronen Aufrufen](setting-security-on-an-asynchronous-call.md) haben Sicherheitsrisiken, sodass Client Anwendungen [Zugriffs Überprüfungen durchführen](performing-access-checks.md) müssen, um sicherzustellen, dass der Rückruf von einer vertrauenswürdigen Quelle aus erfolgt. Clients müssen [temporäre und permanente Ereignisconsumer](securing-wmi-events.md)sichern.

Ein Anbieter kann [Zugriffs Überprüfungen durchführen](performing-access-checks.md) , um sicherzustellen, dass auf die erstellten Ressourcen nur von den entsprechenden Clients zugegriffen wird.

Sowohl Anbieter als auch Clients können die Sicherheit für eine [bestimmte Proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) Verbindung festlegen. Beide können auch [Berechtigungen](executing-privileged-operations.md)aktivieren. Ein Ereignis Anbieter muss sicherstellen, dass der clientconsumer über Berechtigungen zum [empfangen eines angeforderten Ereignisses](providing-events-securely.md)verfügt.

Ein Client oder Anbieter muss möglicherweise eine Remote Verbindung herstellen, die einen anderen Authentifizierungsdienst erfordert, z. b. NTLM anstelle von Kerberos.

 

 



