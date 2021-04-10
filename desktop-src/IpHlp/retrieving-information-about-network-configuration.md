---
description: IP-Hilfsobjekt enthält Informationen zur Netzwerkkonfiguration des lokalen Computers.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Abrufen von Informationen zur Netzwerkkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960645"
---
# <a name="retrieving-information-about-network-configuration"></a>Abrufen von Informationen zur Netzwerkkonfiguration

IP-Hilfsobjekt enthält Informationen zur Netzwerkkonfiguration des lokalen Computers. Um allgemeine Konfigurationsinformationen abzurufen, verwenden Sie die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion. Diese Funktion gibt Informationen zurück, die nicht spezifisch für einen bestimmten Adapter oder eine bestimmte Schnittstelle sind. Beispielsweise gibt **getnetworkparameams** eine Liste der DNS-Server zurück, die vom lokalen Computer verwendet werden.

-   Codebeispiele, die [**getnetworkparser**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) betreffen, finden [Sie unter Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md)Metern.

 

 



