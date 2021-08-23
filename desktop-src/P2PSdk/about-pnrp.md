---
description: Der PNRP-Namespaceanbieter (Peer Name Resolution Protocol) ist eine serverlose Namensauflösungstechnologie, mit der Knoten sich gegenseitig entdecken können.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Informationen zu PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50023fe48d0cd0dc28fae91174942e03dc9df513732378888df0f53242d09f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119338170"
---
# <a name="about-pnrp"></a>Informationen zu PNRP

Der PNRP-Namespaceanbieter (Peer Name Resolution Protocol) ist eine serverlose Namensauflösungstechnologie, mit der Knoten sich gegenseitig entdecken können. PNRP verwendet die Winsock 2-Namespaceanbieter-API.

IPv6-Unterstützung ist für PNRP erforderlich und ist das einzige in der API native Internetprotokoll. PNRP kann jedoch IPv4-Adressen über die 6to4- oder [Teredo-Übergangstechnologien](/windows/desktop/Teredo/portal) auflösen. Windows Benutzer von XP mit Service Pack 1 (SP1) müssen das [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) herunterladen, um die für PNRP erforderliche IPv6-Unterstützung zu aktivieren.

> [!Note]  
> Anwendungen, die PNRP in einer Umgebung mit einer Firewall verwenden, erfordern Ausnahmegruppen, die den anwendungsspezifischen Port abdecken, sowie port "3540-UDP" für PNRP. Diese Ausnahmegruppen sollten immer aktiviert werden, wenn die Anwendung ausgeführt wird.

 

PNRP 2.0 ist zwar auf den Plattformen Windows Vista und Windows Server 2008 nativ, Windows XP-Benutzer müssen jedoch Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) herunterladen, um ein Upgrade auf PNRP 2.0 durchführen zu können.

 

 
