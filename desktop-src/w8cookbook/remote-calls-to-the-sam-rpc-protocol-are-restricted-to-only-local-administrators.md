---
title: Remoteaufrufe des SAM RPC-Protokolls sind nur auf lokale Administratoren beschränkt.
description: Das SAM RPC-Protokoll wird eingeschränkt. Dies bedeutet, dass nur Mitglieder der lokalen Administratorgruppe Remoteaufrufe für Methoden in diesem Protokoll ausführen können. Das Verhalten des Active Directory-Domänencontrollers ist nicht betroffen.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211335"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Remoteaufrufe des SAM RPC-Protokolls sind nur auf lokale Administratoren beschränkt.

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Das SAM RPC-Protokoll wird eingeschränkt. Dies bedeutet, dass nur Mitglieder der lokalen Administratorgruppe Remoteaufrufe für Methoden in diesem Protokoll ausführen können. Das Verhalten des Active Directory-Domänencontrollers ist nicht betroffen.

## <a name="mitigations"></a>Gegenmaßnahmen

Stellen Sie sicher, dass die richtigen Benutzer auf dem PC als Administratoren festgelegt sind. Die für die Zugriffsüberprüfung verwendete Zugriffssteuerungsliste kann über eine Gruppenrichtlinie konfiguriert werden.

 

 




