---
description: Security Support Provider Interface (SSPI) ermöglicht einer Anwendung die Verwendung verschiedener Sicherheitsmodelle, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem zu ändern.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: SSPI-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5d915a8937f57105e2478b41955cc5789fba25791e7f118a84dc4fa38e12fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916817"
---
# <a name="sspi-model"></a>SSPI-Modell

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) ermöglicht einer Anwendung die Verwendung verschiedener Sicherheitsmodelle, die auf einem Computer oder Netzwerk verfügbar sind, ohne die Schnittstelle zum Sicherheitssystem zu ändern. SSPI legt keine Anmeldeinformationen [*fest,*](../secgloss/c-gly.md) da dies im Allgemeinen ein privilegierter Vorgang ist, der vom Betriebssystem verarbeitet wird.

Ein [*Sicherheitssupportanbieter*](../secgloss/s-gly.md) (Security Support Provider, SSP) ist in einer Dll [](../secgloss/s-gly.md) [*(Dynamic Link Library)*](../secgloss/d-gly.md) enthalten, die SSPI implementiert, indem mindestens ein Sicherheitspaket für Anwendungen verfügbar ist. Jedes Sicherheitspaket stellt Zuordnungen zwischen den SSPI-Funktionsaufrufen einer Anwendung und den Funktionen eines tatsächlichen Sicherheitsmodells zur Verfügung. Sicherheitspakete unterstützen [*Sicherheitsprotokolle wie*](../secgloss/s-gly.md) [*Kerberos-Authentifizierung*](../secgloss/k-gly.md) und LAN-Manager.

Die SSPI-Schnittstelle ist im Kernelmodus sowie im Benutzermodus verfügbar. Um die SSPI-Funktionalität im Kernelmodus zu verwenden, müssen Sie das Windows Installable File System DDK installieren. Das aufrufende Modell bleibt unverändert, aber Überlegungen zum Kernelmodus sind auf Funktionsverweisseiten angegeben. Weitere Informationen finden Sie unter [SSPI Functions ( SSPI-Funktionen](authentication-functions.md)).

 

 
