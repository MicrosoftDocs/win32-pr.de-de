---
description: COPP-Abfragereferenz
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: COPP-Abfragereferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d36cde152600faaa1dd567faac916bfa8281e2b2edb9464074fe34a58d5011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909660"
---
# <a name="copp-query-reference"></a>COPP-Abfragereferenz

In diesem Abschnitt werden die Statusabfragen beschrieben, die vom Certified Output Protection Protocol (COPP) unterstützt werden. Für jede Abfrage wird die GUID, die die Abfrage definiert, zusammen mit den Eingabe- und Rückgabedaten aufgeführt.



| Abfrage                   | GUID                                     |
|-------------------------|------------------------------------------|
| Busdaten                | **DXVA \_ COPPQueryBusData**               |
| Connectortyp          | **DXVA \_ COPPQueryConnectorType**         |
| Anzeigen von Daten            | **DXVA \_ COPPQueryDisplayData**           |
| HDCP-Schlüsseldaten           | **DXVA \_ COPPQueryHDCPKeyData**           |
| Globale Schutzebene | **DXVA \_ COPPQueryGlobalProtectionLevel** |
| Lokale Schutzebene  | **DXVA \_ COPPQueryLocalProtectionLevel**  |
| Schutztyp         | **DXVA \_ COPPQueryProtectionType**        |
| Signaling               | **DXVA \_ COPPQuerySignaling**             |



 

Busdatenabfrage

Gibt den Typ des E/A-Bus zurück, der vom Grafikadapter verwendet wird.

-   **GUID:** DXVA \_ COPPQueryBusData
-   **Eingabedaten:** Keine.
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-COPPStatusData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) zurück. Der Bustyp wird im **dwData-Member** als Flag von der [**COPP \_ BusType-Enumeration**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) zurückgegeben.

Connectortypabfrage

Gibt den physischen Connectortyp zurück.

-   **GUID:** DXVA \_ COPPQueryConnectorType
-   **Eingabedaten:** Keine.
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-COPPStatusData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) zurück. Der Connectortyp wird im **dwData-Member** als Flag von der [**COPP \_ ConnectorType-Enumeration**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) zurückgegeben.

Datenabfrage anzeigen

Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.

Das Videosignal, das über den Connector übertragen wird, hat nicht unbedingt das gleiche Format wie der Desktopanzeigemodus. Der Desktopanzeigemodus kann beispielsweise 1024 x 768 Pixel bei 85 Hz betragen, während der Connector ein S-Video-Connector sein kann, der ein Videosignal mit 720 x 480 Pixeln und 60/1,01 Hz-Interlacing überträgt. In diesem Fall gibt der Treiber die Auflösung des S-Video-Signals zurück, nicht die Desktopauflösung.

-   **GUID:** DXVA \_ COPPQueryDisplayData
-   **Eingabedaten:** Keine.
-   **Rückgabedaten:** Gibt eine [**DXVA \_ COPPStatusDisplayData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) zurück.

HDCP-Schlüsseldatenabfrage

Gibt den HDCP-Schlüsselauswahlvektor (B-KSV) des Geräts zurück.

Die KSV ist ein Bezeichner, der dem Gerätehersteller bereitgestellt wird und bei der HDCP-Authentifizierung und -Einrichtung verwendet wird. Die Anwendung sollte diesen Wert mit der Liste der gesperrten KSVs überprüfen. Der Mechanismus zum Abrufen der KSV-Sperrliste liegt außerhalb des Bereichs des COPP-Protokolls. Weitere Informationen finden Sie in der HDCP-Spezifikation.

Diese Abfrage bestimmt auch, ob das verbundene HDCP-Gerät ein Monitor oder ein HDCP-Repeater ist. Die Anwendung sollte keine geschützten Inhalte wieder geben, wenn das HDCP-Gerät ein HDCP-Repeater ist, da diese von COPP nicht unterstützt werden.

-   **GUID:** DXVA \_ COPPQueryHDCPKeyData
-   **Eingabedaten:** Keine.
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-STRUKTUR COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) zurück.

Abfrage auf globaler Schutzebene

Gibt die globale Schutzebene für einen angegebenen Schutzmechanismus zurück.

Die globale Schutzebene ist die Schutzebene, die derzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden. Beispielsweise kann eine Anwendung die ACP-Schutzebene festlegen, indem sie die **ChangeDisplaySettingsEx-Funktion** aufruft. In diesem Fall würde die globale Schutzebene diese Einstellung widerspiegeln, obwohl sie nicht über COPP angefordert wurde.

-   **GUID:** DXVA \_ COPPQueryGlobalProtectionLevel
-   **Eingabedaten:** Der zu abfragende Schutzmechanismus, angegeben als 32-Bit-Ganzzahl. Weitere Informationen [finden Sie unter COPP-Schutztypflags](copp-protection-type-flags.md).
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-COPPStatusData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) zurück. Die aktuelle Schutzebene wird im **dwData-Element** zurückgegeben. Die Bedeutung dieses Werts hängt vom abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert des **dwData-Mitglieds** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle gezeigt.

    | Schutzmechanismus | Enumeration                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ \_ \_ ACP-Schutzebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_COPP-CGMSA-Schutzebene \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**COPP \_ \_ HDCP-Schutzebene \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Abfrage auf lokaler Schutzebene

Gibt die lokale Schutzebene für einen angegebenen Schutzmechanismus zurück.

Die lokale Schutzebene ist die Schutzebene, die über die aktuelle COPP-Sitzung angefordert wurde. Der Treiber kann eine höhere Schutzebene festlegen.

-   **GUID:** DXVA \_ COPPQueryLocalProtectionLevel
-   **Eingabedaten:** Der abfragte Schutzmechanismus als 32-Bit-Ganzzahl. Weitere Informationen [finden Sie unter COPP-Schutztypflags](copp-protection-type-flags.md).
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-COPPStatusData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) zurück. Die aktuelle Schutzebene wird im **dwData-Element** zurückgegeben. Die Bedeutung dieses Werts hängt vom abgefragten Schutzmechanismus ab. Für jeden Schutzmechanismus ist der Wert des **dwData-Mitglieds** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle gezeigt.

    | Schutzmechanismus | Enumeration                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ \_ \_ ACP-Schutzebene**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_COPP-CGMSA-Schutzebene \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | Hdcp                 | [**COPP \_ \_ HDCP-Schutzebene \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Schutztypabfrage

Gibt die Schutzmechanismen zurück, die für den Connector verfügbar sind.

-   **GUID:** DXVA \_ COPPQueryProtectionType
-   **Eingabedaten:** Keine.
-   **Rückgabedaten:** Gibt eine [**\_ DXVA-COPPStatusData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) zurück. Die Schutzmechanismen werden im **dwData-Element** als Kombination aus 0 (null) oder mehr Flags zurückgegeben. Weitere Informationen [finden Sie unter COPP-Schutztypflags](copp-protection-type-flags.md). Wenn mehr als ein Schutzmechanismus verfügbar ist, werden die Flags mit einem bitweisen **OR** kombiniert.

Signalisierungsabfrage

Gibt eine Liste aller Schutzstandards zurück, die vom Treiber unterstützt werden, den derzeit aktiven Standard und das aktuelle Seitenverhältnis oder andere Signaldaten.

-   **GUID:** DXVA \_ COPPQuerySignaling
-   **Eingabedaten:** Keine.
-   **Daten zurückgeben:** Gibt eine [**\_ DXVA-COPPStatusSignalingCmdData-Struktur**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



