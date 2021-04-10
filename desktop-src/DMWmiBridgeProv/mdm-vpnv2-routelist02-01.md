---
title: MDM_VPNv2_RouteList02_01-Klasse
description: Die MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse enthält eine optionale Liste der Routen, die der Routing Tabelle für die VPN-Schnittstelle hinzugefügt werden sollen.
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
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040827"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse enthält eine optionale Liste der Routen, die der Routing Tabelle für die VPN-Schnittstelle hinzugefügt werden sollen.

Dies ist erforderlich, wenn die VPN-Serversite über mehr Subnetze verfügt, die auf der IP-Adresse basieren, die der Schnittstelle zugeordnet ist.

Alle Computer, auf denen TCP/IP ausgeführt wird, treffen Routing Entscheidungen. Diese Entscheidungen werden von der IP-Routing Tabelle gesteuert. Durch das Hinzufügen von Werten unter diesem Knoten wird die Routing Tabelle mit Routen für die VPN-Schnittstelle nach Verbindung aktualisiert. Die Werte unter diesem Knoten stellen das Ziel Präfix von IP-Routen dar. Ein Ziel Präfix besteht aus einem IP-Adress Präfix und einer Präfix Länge.

Wenn Sie hier eine Route hinzufügen, kann der Netzwerk Stapel den Datenverkehr ermitteln, der über die VPN-Schnittstelle für Split-Tunnel-VPN geleitet werden muss. Einige VPN-Server können dies während der Verbindungs Verhandlung konfigurieren und benötigen diese Informationen nicht im VPN-Profil. Wenden Sie sich an den VPN-Server Administrator, um zu ermitteln, ob Sie diese Informationen im VPN-Profil benötigen.

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

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Adresse](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/RouteList".

</dd> <dt>

[Prefixsize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

