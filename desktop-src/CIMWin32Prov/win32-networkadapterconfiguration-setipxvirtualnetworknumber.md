---
description: Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Die Methode "stipxvirtualnetworknumber" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344624"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Die Methode "stipxvirtualnetworknumber" der Win32 \_ networkadapterconfiguration-Klasse

Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest. Für Windows 2000 und Windows NT 3,51 oder höher wird eine interne Netzwerk Nummer für das interne Routing verwendet. Die interne Netzwerk Nummer wird auch als virtuelle Netzwerk Nummer bezeichnet. Das Computersystem im Netzwerk wird eindeutig identifiziert. Die-Methode gibt einen ganzzahligen Wert zurück, der wie folgt interpretiert werden kann:

## <a name="syntax"></a>Syntax


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPXVirtualNetNumber* \[ in\]
</dt> <dd>

Die Nummer des virtuellen Netzwerks für dieses System.

</dd> </dl>

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

 

 




