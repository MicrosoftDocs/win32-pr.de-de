---
title: Remote Aufrufe des Sam RPC-Protokolls sind nur auf lokale Administratoren beschränkt.
description: Das Sam-RPC-Protokoll wird eingeschränkt. Dies bedeutet, dass nur Mitglieder der lokalen Administrator Gruppe Remote Aufrufe für Methoden in diesem Protokoll durchführen können. Active Directory Domänen Controller Verhalten ist nicht betroffen.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100818"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Remote Aufrufe des Sam RPC-Protokolls sind nur auf lokale Administratoren beschränkt.

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Das Sam-RPC-Protokoll wird eingeschränkt. Dies bedeutet, dass nur Mitglieder der lokalen Administrator Gruppe Remote Aufrufe für Methoden in diesem Protokoll durchführen können. Active Directory Domänen Controller Verhalten ist nicht betroffen.

## <a name="mitigations"></a>Gegenmaßnahmen

Stellen Sie sicher, dass die richtigen Benutzer auf dem PC als Administratoren festgelegt sind. Die für die Zugriffs Überprüfung verwendete ACL ist über die Gruppenrichtlinie konfigurierbar.

 

 




