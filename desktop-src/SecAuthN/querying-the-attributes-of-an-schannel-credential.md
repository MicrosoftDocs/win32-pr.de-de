---
description: Stellt SChannel-spezifische Informationen über Anmelde Informationen bereit.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Abfragen der Attribute von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215881"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Abfragen der Attribute von SChannel-Anmelde Informationen

Die [**querykredentialsattributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) -Funktion stellt SChannel-spezifische Informationen über Anmelde Informationen bereit. Diese Informationen werden ursprünglich angegeben, wenn die Anmelde Informationen erstellt werden. Weitere Informationen finden Sie unter Abrufen von [SChannel-Anmelde](obtaining-schannel-credentials.md)Informationen. Die von dieser Funktion gemeldeten Informationen sind für alle Verbindungen ([*Sicherheits Kontexte*](../secgloss/s-gly.md)) gültig, die mit den angegebenen Anmelde Informationen erstellt wurden.

 

 
