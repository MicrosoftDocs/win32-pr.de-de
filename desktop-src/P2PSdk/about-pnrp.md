---
description: Der PNRP (Peer Name Resolution Protocol)-Namespace Anbieter (NSP) ist eine Server lose namens Auflösungs Technologie, die es Knoten ermöglicht, sich gegenseitig zu ermitteln.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Informationen zu PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131701"
---
# <a name="about-pnrp"></a>Informationen zu PNRP

Der PNRP (Peer Name Resolution Protocol)-Namespace Anbieter (NSP) ist eine Server lose namens Auflösungs Technologie, die es Knoten ermöglicht, sich gegenseitig zu ermitteln. PNRP verwendet die-Namespace Anbieter-API von Winsock 2.

Die IPv6-Unterstützung ist für PNRP erforderlich und ist das einzige Internet Protokoll, das der API eigen ist. Allerdings kann PNRP IPv4-Adressen über die IPv6-zu-IPv4-oder [Teredo](/windows/desktop/Teredo/portal) -Übergangs Technologien auflösen. Benutzer von Windows XP mit Service Pack 1 (SP1) müssen das [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) herunterladen, um die von PNRP benötigte IPv6-Unterstützung zu aktivieren.

> [!Note]  
> Anwendungen, die PNRP in einer Umgebung mit einer Firewall verwenden, benötigen Ausnahme Gruppen, die den für die Anwendung spezifischen Port abdecken, sowie den Port "3540-UDP" für PNRP. Diese Ausnahme Gruppen sollten immer dann aktiviert werden, wenn die Anwendung ausgeführt wird.

 

Obwohl PNRP 2,0 auf den Plattformen Windows Vista und Windows Server 2008 einheitlich ist, müssen Windows XP-Benutzer Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) herunterladen, um ein Upgrade auf PNRP 2,0 durchzuführen.

 

 
