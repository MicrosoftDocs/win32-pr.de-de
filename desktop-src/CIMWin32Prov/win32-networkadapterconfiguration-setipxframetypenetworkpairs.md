---
description: Legt die IPX-Netzwerknummern-/Framepaare (Internetworking Packet Exchange) für diesen Netzwerkadapter fest.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: SetIPXFrameTypeNetworkPairs-Methode der Win32_NetworkAdapterConfiguration-Klasse
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
ms.openlocfilehash: f914f996e26d64ae66c0be2acf1dee3988ccc2015109c6e7d3b340b406c0c23e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973025"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>SetIPXFrameTypeNetworkPairs-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Legt die IPX-Netzwerknummern-/Framepaare (Internetworking Packet Exchange) für diesen Netzwerkadapter fest.

Windows 2000 und Windows NT 3.51 und höher verwenden eine IPX-Netzwerknummer für Routingzwecke. Sie wird jeder konfigurierten Kombination aus Frametyp und Netzwerkadapter auf Ihrem Computersystem zugewiesen. Diese Zahl wird manchmal als "externe Netzwerknummer" bezeichnet. Er muss für jedes Netzwerksegment eindeutig sein. Wenn der Frametyp auf AUTO festgelegt ist, sollte die Netzwerknummer auf 0 (null) festgelegt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPXNetworkNumber* \[ In\]
</dt> <dd>

Ein Array von Zeichen, die einen Adapter auf dem Computersystem eindeutig identifizieren. Der NetWare Link(NWLink) IPX/SPX-kompatible Transport in Windows 2000 und Windows NT 3.51 oder höher verwendet zwei verschiedene Arten von Netzwerknummern. Diese Zahl wird manchmal auch als externe Netzwerknummer bezeichnet. Er muss für jedes Netzwerksegment eindeutig sein. Die Werte in dieser Zeichenfolgenliste müssen über einen entsprechenden Wert im IPXFrameType-Parameter verfügen, der den für dieses Netzwerk verwendeten Paketrahmentyp identifiziert.

</dd> <dt>

*IPXFrameType* \[ In\]
</dt> <dd>

Ein ganzzahliges Array von Frametypbezeichnern. Die Werte in diesem Array entsprechen den Elementen im *IPXNetworkNumber-Parameter.*

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet SNAP** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>

**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)
</dt> <dt>

**Erfolgreicher Abschluss, Neustart erforderlich** (1)
</dt> <dt>

**Methode wird auf dieser Plattform nicht unterstützt** (64)
</dt> <dt>

**Unbekannter Fehler** (65)
</dt> <dt>

**Ungültige Subnetzmaske** (66)
</dt> <dt>

**Fehler beim Verarbeiten einer zurückgegebenen Instanz** (67)
</dt> <dt>

**Ungültiger Eingabeparameter** (68)
</dt> <dt>

**Mehr als 5 angegebene Gateways** (69)
</dt> <dt>

**Ungültige IP-Adresse** (70)
</dt> <dt>

**Ungültige Gateway-IP-Adresse** (71)
</dt> <dt>

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72)
</dt> <dt>

**Ungültiger Domänenname** (73)
</dt> <dt>

**Ungültiger Hostname** (74)
</dt> <dt>

**Kein primärer/sekundärer WINS-Server definiert** (75)
</dt> <dt>

**Ungültige Datei** (76)
</dt> <dt>

**Ungültiger Systempfad** (77)
</dt> <dt>

**Fehler beim Kopieren** der Datei (78)
</dt> <dt>

**Ungültiger Sicherheitsparameter** (79)
</dt> <dt>

**TCP/IP-Dienst kann nicht konfiguriert** werden (80)
</dt> <dt>

**DHCP-Dienst kann nicht konfiguriert werden** (81)
</dt> <dt>

**DHCP-Lease kann nicht erneuert werden** (82)
</dt> <dt>

**DHCP-Lease kann nicht veröffentlicht werden** (83)
</dt> <dt>

**IP auf Adapter nicht aktiviert** (84)
</dt> <dt>

**IPX für Adapter nicht aktiviert** (85)
</dt> <dt>

**Frame-/Netzwerknummern-Begrenzungsfehler** (86)
</dt> <dt>

**Ungültiger Frametyp** (87)
</dt> <dt>

**Ungültige Netzwerknummer** (88)
</dt> <dt>

**Doppelte Netzwerknummer** (89)
</dt> <dt>

**Parameter außerhalb der Grenzen** (90)
</dt> <dt>

**Zugriff verweigert** (91)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (92)
</dt> <dt>

**Bereits vorhanden** (93)
</dt> <dt>

**Pfad, Datei oder Objekt nicht gefunden** (94)
</dt> <dt>

**Dienst kann nicht benachrichtigt werden** (95)
</dt> <dt>

**DNS-Dienst kann nicht benachrichtigt werden** (96)
</dt> <dt>

**Schnittstelle nicht konfigurierbar** (97)
</dt> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98)
</dt> <dt>

**DHCP auf Adapter nicht aktiviert** (100)
</dt> <dt>

**Sonstige** (101–4294967295)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




