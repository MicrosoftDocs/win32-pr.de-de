---
title: Richtlinien für das Schreiben von EAP-DLLs
description: Sie können EAP-DLLs oder-Plug-ins schreiben, um die Leistung in verschiedenen Szenarien zu optimieren.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106340677"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Richtlinien für das Schreiben von EAP-DLLs

Sie können EAP-DLLs oder-Plug-ins schreiben, um die Leistung in verschiedenen Szenarien zu optimieren.

## <a name="general-guidelines"></a>Allgemeine Richtlinien

-   Um eine verschlüsselte Verbindung zu erstellen, müssen die EAP-Plug-ins Verschlüsselungsschlüssel generieren und über die herstellerspezifischen RADIUS-Attribute von Microsoft, MS-MPPE-Send-Keys und MS-MPPE-Recv-Keys, zurückgeben. Weitere Informationen finden Sie im Abschnitt "Hinweise" in der [**PPP- \_ EAP- \_ Ausgabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .

## <a name="wireless-guidelines"></a>Drahtlos Richtlinien

Im folgenden finden Sie Richtlinien und Empfehlungen zum Schreiben eines EAP-Plug-ins, das das Authentifizieren von Computern in drahtlosen Szenarios (802.1 x) unterstützt. Dieser Abschnitt gilt nicht für VPN-und einwählszenarien.

-   Damit die Ausführung von unbeaufsichtigten Systemen nicht blockiert wird, dürfen keine Benutzeroberflächen Aufrufe von EAP-Plug-Ins ausgeführt werden.
-   Die EAP-Plug-in-Implementierung des Computers zur Computer Authentifizierung muss so schnell wie möglich ausgeführt werden, sodass der Start des Betriebssystems nicht beeinträchtigt wird.
    > [!Note]  
    > Wenn das EAP-Protokoll keine Computer Authentifizierung unterstützt, muss es das computerauthentifizierungsflag, die **RAS- \_ EAP- \_ Flag- \_ Computer \_** Authentifizierung, die im Feld **fFlags** in der [**PPP- \_ EAP- \_ Eingabe**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)verwendet wird, überprüfen und einen Fehler zurückgeben.

     

 

 




