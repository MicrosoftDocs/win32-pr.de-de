---
description: Nachdem Sie Den Netzwerkanbieter oder Anmeldeinformations-Manager erstellt haben, müssen Sie ihn beim System registrieren.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrieren von Netzwerkanbietern und Anmeldeinformations-Managern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec3b3eff5fc396a112986d8c736dba095701a02ffb9e72c21422b83e3596235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919588"
---
# <a name="registering-network-providers-and-credential-managers"></a>Registrieren von Netzwerkanbietern und Anmeldeinformations-Managern

Nachdem Sie Den Netzwerkanbieter oder Anmeldeinformations-Manager erstellt haben, müssen Sie ihn beim System registrieren. Dies ist erforderlich, damit der MPR weiß, welche Netzwerkanbieter installiert sind. Wenn der MPR gestartet wird, überprüft er die Registrierung und lädt alle gefundenen Netzwerkanbieter oder Anmeldeinformations-Manager.

Da Netzwerkanbieter und Anmeldeinformations-Manager verknüpft sind, werden sie in den gleichen Unterschlüsseln der Registrierung registriert. Tatsächlich können Netzwerkanbieter-DLLs auch Anmeldeinformations-Manager sein.

Ausführliche Informationen zu den Registrierungsschlüsseln, die Sie für Ihren Netzwerkanbieter oder Anmeldeinformations-Manager erstellen sollten, finden Sie unter [Authentifizierungsregistrierungsschlüssel.](authentication-registry-keys.md)

 

 



