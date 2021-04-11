---
description: Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Die Methode "setxframetypetworkpairs" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127472"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Die Methode "setxframetypetworkpaars" der Win32- \_ Klasse "networkadapterconfiguration"

Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.

Windows 2000 und Windows NT 3,51 und höher verwenden eine IPX-Netzwerk Nummer für Routing Zwecke. Sie wird den einzelnen konfigurierten Frame Typen/Netzwerkadaptern auf dem Computersystem zugewiesen. Diese Zahl wird manchmal auch als "externe Netzwerk Nummer" bezeichnet. Er muss für jedes Netzwerksegment eindeutig sein. Wenn der Frame-Typ auf "Auto" festgelegt ist, muss die Netzwerk Nummer 0 (null) lauten.

## <a name="syntax"></a>Syntax


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPXNetworkNumber* \[ in\]
</dt> <dd>

Ein Array von Zeichen, die einen Adapter im Computersystem eindeutig identifizieren. Der IPX/SPX-kompatible Transport (NetWare Link) in Windows 2000 und Windows NT 3,51 oder höher verwendet zwei unterschiedliche Arten von Netzwerk Nummern. Diese Zahl wird mitunter auch als externe Netzwerk Nummer bezeichnet. Er muss für jedes Netzwerksegment eindeutig sein. Die Werte in dieser Zeichen folgen Liste müssen über einen entsprechenden Wert im IPXFrameType-Parameter verfügen, der den für dieses Netzwerk verwendeten Pakettyp identifiziert.

</dd> <dt>

*IPXFrameType* \[ in\]
</dt> <dd>

Ein ganzzahliges Array von Frame-typbezeichgern. Die Werte in diesem Array entsprechen den Elementen im *IPXNetworkNumber* -Parameter.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet-Snap** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Auto** (255)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>

**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)
</dt> <dt>

**Erfolgreicher Abschluss, Neustart erforderlich** (1)
</dt> <dt>

**Methode wird auf dieser Plattform nicht unterstützt** (64).
</dt> <dt>

**Unbekannter Fehler** (65).
</dt> <dt>

**Ungültige Subnetzmaske** (66).
</dt> <dt>

**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde** (67).
</dt> <dt>

**Ungültiger Eingabeparameter** (68)
</dt> <dt>

**Es wurden mehr als 5 Gateways angegeben** (69).
</dt> <dt>

**Ungültige IP-Adresse** (70)
</dt> <dt>

**Ungültige Gateway-IP-Adresse** (71)
</dt> <dt>

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72).
</dt> <dt>

**Ungültiger Domänen Name** (73).
</dt> <dt>

**Ungültiger Hostname** (74).
</dt> <dt>

**Kein primärer/sekundärer WINS-Server definiert** (75)
</dt> <dt>

**Ungültige Datei** (76)
</dt> <dt>

**Ungültiger Systempfad** (77).
</dt> <dt>

Fehler beim **Kopieren der Datei** (78).
</dt> <dt>

**Ungültiger Sicherheitsparameter** (79).
</dt> <dt>

Der **TCP/IP-Dienst kann nicht konfiguriert** werden (80).
</dt> <dt>

**DHCP-Dienst kann nicht konfiguriert** werden (81).
</dt> <dt>

**DHCP-Lease kann nicht erneuert** werden (82).
</dt> <dt>

**DHCP-Lease kann nicht frei** gegeben werden (83).
</dt> <dt>

Die **IP ist auf dem Adapter nicht aktiviert** (84).
</dt> <dt>

**IPX ist auf dem Adapter nicht aktiviert** (85).
</dt> <dt>

**Fehler bei Frame/Netzwerk Nummer** (86)
</dt> <dt>

**Ungültiger Frame-Typ** (87).
</dt> <dt>

**Ungültige Netzwerk Nummer** (88).
</dt> <dt>

**Doppelte Netzwerk Nummer** (89)
</dt> <dt>

**Parameter außerhalb des** gültigen Bereichs (90)
</dt> <dt>

**Zugriff verweigert** (91)
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (92)
</dt> <dt>

**Bereits vorhanden** (93)
</dt> <dt>

Der **Pfad, die Datei oder das Objekt wurde nicht gefunden** (94).
</dt> <dt>

Der **Dienst kann nicht benachrichtigt** werden (95).
</dt> <dt>

Der **DNS-Dienst kann nicht benachrichtigt** werden (96).
</dt> <dt>

**Schnittstelle nicht konfigurierbar** (97)
</dt> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98).
</dt> <dt>

**DHCP ist auf dem Adapter nicht aktiviert** (100).
</dt> <dt>

**Sonstige** (101 – 4294967295)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




