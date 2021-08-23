---
title: MDM_VPNv2_RouteList02_01-Klasse
description: Die MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse enthält eine optionale Liste von Routen, die der Routingtabelle für die VPN-Schnittstelle hinzugefügt werden sollen.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01-Klasse
- MDM_VPNv2_RouteList02_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ea9725d70d3acfe4e6831d1d386aedecfd9374728b103d50b67aa15cb61ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750270"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse** enthält eine optionale Liste von Routen, die der Routingtabelle für die VPN-Schnittstelle hinzugefügt werden sollen.

Dies ist für den Fall der aufteilungsbasierten Tunnelung erforderlich, wenn der VPN-Serverstandort mehr Subnetze aufwies, als das Standardsubnetz basierend auf der IP-Adresse, die der Schnittstelle zugewiesen ist.

Jeder Computer, auf dem TCP/IP ausgeführt wird, trifft Routingentscheidungen. Diese Entscheidungen werden durch die IP-Routingtabelle gesteuert. Durch das Hinzufügen von Werten unter diesem Knoten wird die Routingtabelle mit Routen für die VPN-Schnittstelle nach der Verbindung aktualisiert. Die Werte unter diesem Knoten stellen das Zielpräfix von IP-Routen dar. Ein Zielpräfix besteht aus einem IP-Adresspräfix und einer Präfixlänge.

Wenn Sie hier eine Route hinzufügen, kann der Netzwerkstapel den Datenverkehr identifizieren, der über die VPN-Schnittstelle für ein VPN mit geteilten Tunneln geleitet werden muss. Einige VPN-Server können dies während der Verbindungsaushandlung konfigurieren und benötigen diese Informationen nicht im VPN-Profil. Wenden Sie sich an Ihren VPN-Serveradministrator, um zu ermitteln, ob Sie diese Informationen im VPN-Profil benötigen.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Member

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[Adresse](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList".

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

