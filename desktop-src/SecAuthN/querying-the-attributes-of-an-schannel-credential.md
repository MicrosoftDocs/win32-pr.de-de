---
description: Stellt Schannel-spezifische Informationen zu Anmeldeinformationen bereit.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Abfragen der Attribute von Schannel-Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa940e6214f23a69af2e0f7de58813e007129caadac46be8a6c436b8d62094f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919909"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Abfragen der Attribute von Schannel-Anmeldeinformationen

Die [**QueryCredentialsAttributes-Funktion**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) stellt Schannel-spezifische Informationen zu Anmeldeinformationen bereit. Diese Informationen werden ursprünglich beim Erstellen der Anmeldeinformationen angegeben. Weitere Informationen finden Sie unter [Abrufen von Schannel-Anmeldeinformationen.](obtaining-schannel-credentials.md) Die von dieser Funktion gemeldeten Informationen sind für alle Verbindungen [*(Sicherheitskontexte)*](../secgloss/s-gly.md)gültig, die mit den angegebenen Anmeldeinformationen erstellt wurden.

 

 
