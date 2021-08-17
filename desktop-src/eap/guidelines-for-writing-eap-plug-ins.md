---
title: Richtlinien zum Schreiben von EAP-DLLs
description: EAP-DLLs oder Plug-Ins können geschrieben werden, um ihre Leistung in verschiedenen Szenarien zu optimieren.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c786da1ca026039ffd052f1213b2904dbfa602ee67c6d74aed7a0fe11fd9d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499155"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Richtlinien zum Schreiben von EAP-DLLs

EAP-DLLs oder Plug-Ins können geschrieben werden, um ihre Leistung in verschiedenen Szenarien zu optimieren.

## <a name="general-guidelines"></a>Allgemeine Richtlinien

-   Um eine verschlüsselte Verbindung zu erstellen, müssen EAP-Plug-Ins Verschlüsselungsschlüssel generieren und über die microsoft-anbieterspezifischen RADIUS-Attribute MS-MPPE-Send-Keys und MS-MPPE-Recv-Keys zurückgeben. Weitere Informationen finden Sie im Abschnitt "Hinweise" in [**DER \_ EAP \_ OUTPUT-Ausgabe.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)

## <a name="wireless-guidelines"></a>Drahtlosrichtlinien

Im Folgenden finden Sie Richtlinien und Empfehlungen zum Schreiben eines EAP-Plug-Ins, das die Authentifizierung von Computern in Drahtlosszenarien (802.1X) unterstützt. Dieser Abschnitt gilt nicht für VPN- und DFÜ-Szenarien.

-   Um die Ausführung unbeaufsichtigter Systeme nicht zu blockieren, dürfen EAP-Plug-Ins keine Benutzeroberflächenaufrufe ausführen.
-   Die EAP-Plug-In-Implementierung des Computerauthentifizierungsschritts muss so schnell wie möglich abgeschlossen werden, damit der Start des Betriebssystems nicht beeinträchtigt wird.
    > [!Note]  
    > Wenn Ihr EAP-Protokoll die Computerauthentifizierung nicht unterstützt, muss es nach dem Computerauthentifizierungsflag **,RAS \_ EAP \_ FLAG MACHINE \_ \_ AUTH,** das im **fFlags-Feld** in [**DER \_ \_ EAP-EINGABE**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)für den Computer verwendet wird, suchen und einen Fehler zurückgeben.

     

 

 




