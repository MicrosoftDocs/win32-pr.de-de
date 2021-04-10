---
description: COPP-Abfrage Verweis
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: COPP-Abfrage Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041305"
---
# <a name="copp-query-reference"></a>COPP-Abfrage Verweis

In diesem Abschnitt werden die Statusabfragen beschrieben, die vom Certified Output Protection Protocol (COPP) unterstützt werden. Für jede Abfrage wird die GUID, die die Abfrage definiert, zusammen mit den Eingabedaten und den Rückgabe Daten aufgelistet.



| Abfrage                   | GUID                                     |
|-------------------------|------------------------------------------|
| Busdaten                | **DXVA- \_ coppquerybusdata**               |
| Connectortyp          | **DXVA " \_ coppqueryconnector Type"**         |
| Anzeigen von Daten            | **DXVA-" \_ coppquerydisplaydata"**           |
| HDCP-Schlüsseldaten           | **DXVA-" \_ coppqueryhdcpkeydata"**           |
| Globale Schutz Ebene | **DXVA- \_ coppqueryglobalschutzlevel** |
| Lokale Schutz Ebene  | **DXVA- \_ coppquerylocalschutzlevel**  |
| Schutztyp         | **DXVA-" \_ coppqueryschutztype"**        |
| Signaling               | **DXVA- \_ coppquerysignalisierung**             |



 

Busdaten Abfrage

Gibt den Typ des e/a-Busses zurück, der vom Grafikadapter verwendet wird.

-   **GUID**: DXVA \_ coppquerybusdata
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück. Der Bustyp wird im **dwdata** -Member als Flag aus der [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) -Enumeration zurückgegeben.

Connector-typabfrage

Gibt den physischen Verbindungstyp zurück.

-   **GUID**: DXVA-" \_ coppqueryconnector Type"
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück. Der connectiontyp wird im **dwdata** -Member als Flag aus der [**COPP \_ Stecker Type**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) -Enumeration zurückgegeben.

Datenabfrage anzeigen

Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.

Das über den Connector übertragene Videosignal weist nicht notwendigerweise dasselbe Format wie der Desktop Anzeigemodus auf. Der Desktop Anzeigemodus kann z. b. 1024 x 768 Pixel um 85 Hz betragen, während der Connector ein S-Video-Connector sein kann, der ein Video Signal mit 720x480 Pixel, 60/1.01 Hz mit Zeilen Sprung überträgt. In diesem Fall würde der Treiber die Auflösung des S-Video Signals und nicht die Desktop Auflösung zurückgeben.

-   **GUID**: DXVA \_ coppquerydisplaydata
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA-Struktur von " \_ coppstatus-displayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) " zurück.

HDCP-Schlüsseldaten Abfrage

Gibt den HDCP-Schlüsselauswahl Vektor (B-KSV) des Geräts zurück.

Der KSV ist ein Bezeichner, der dem Gerätehersteller zur Verfügung gestellt wird und im HDCP-Authentifizierungs-und-Setup Prozess verwendet wird. Die Anwendung sollte diesen Wert mit der Liste der gesperrten ksvs überprüfen. Der Mechanismus zum Abrufen der KSV-Sperr Liste liegt außerhalb des Gültigkeits Bereichs des COPP-Protokolls. Weitere Informationen finden Sie in der HDCP-Spezifikation.

Diese Abfrage bestimmt auch, ob das verbundene HDCP-Gerät ein Monitor oder ein HDCP-Wiederholungs Modul ist. Die Anwendung sollte geschützte Inhalte nicht wiedergeben, wenn das HDCP-Gerät ein HDCP-Repeater ist, da diese nicht von COPP unterstützt werden.

-   **GUID**: DXVA \_ coppqueryhdcpkeydata
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA- \_ coppstatuushdcpkeydata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) -Struktur zurück.

Abfrage der globalen Schutz Ebene

Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.

Die globale Schutz Ebene ist die Schutz Ebene, die zurzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden. Beispielsweise kann eine Anwendung die ACP-Schutz Ebene durch Aufrufen der **changedisplaysettingsex** -Funktion festlegen. In diesem Fall würde die globale Schutz Ebene diese Einstellung widerspiegeln, auch wenn Sie nicht über COPP angefordert wurde.

-   **GUID**: DXVA \_ coppqueryglobalschutzlevel
-   **Eingabedaten**: der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird. Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md).
-   **Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück. Die aktuelle Schutz Ebene wird im **dwdata** -Member zurückgegeben. Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert des **dwdata** -Members ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.

    | Schutzmechanismus | Enumeration                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ -ACP- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**COPP- \_ cgmsa- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**COPP- \_ HDCP- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Abfrage der lokalen Schutz Ebene

Gibt die lokale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.

Die lokale Schutz Ebene ist die Schutz Ebene, die durch die aktuelle COPP-Sitzung angefordert wurde. Der Treiber kann eine höhere Schutz Ebene festlegen.

-   **GUID**: DXVA \_ coppquerylocalschutzlevel
-   **Eingabedaten**: der zu Abfrage Ende Schutzmechanismus als 32-Bit-Ganzzahl. Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md).
-   **Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück. Die aktuelle Schutz Ebene wird im **dwdata** -Member zurückgegeben. Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert des **dwdata** -Members ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.

    | Schutzmechanismus | Enumeration                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ -ACP- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**COPP- \_ cgmsa- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**COPP- \_ HDCP- \_ Schutz \_ Ebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Schutztyp Abfrage

Gibt die Schutzmechanismen zurück, die für den Connector verfügbar sind.

-   **GUID**: DXVA " \_ coppqueryschutztype"
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück. Die Schutzmechanismen werden im **dwdata** -Member als eine Kombination aus null oder mehr Flags zurückgegeben. Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md). Wenn mehr als ein Schutzmechanismus verfügbar ist, werden die Flags mit einem bitweisen **or** kombiniert.

Signalisierungs Abfrage

Gibt eine Liste mit allen Schutzstandards zurück, die vom Treiber unterstützt werden, dem derzeit aktiven Standard und dem aktuellen Seitenverhältnis oder anderen Signalisierungs Daten.

-   **GUID**: DXVA- \_ coppquerysignalisierung
-   **Eingabedaten**: keine.
-   **Return Data**: gibt eine [**DXVA-Struktur von " \_ coppstatuussignalingcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) " zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



