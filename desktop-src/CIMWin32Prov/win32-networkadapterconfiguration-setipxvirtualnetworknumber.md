---
description: Legt die IPX-Nummer (Internetworking Packet Exchange) des virtuellen Netzwerks auf dem Zielcomputersystem fest.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: SetIPXVirtualNetworkNumber-Methode der Win32_NetworkAdapterConfiguration-Klasse
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
ms.openlocfilehash: 37af763450eab2fdba373fe21bfde5c0b4e1e38fda1f42aff59c425ba6b10000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079774"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>SetIPXVirtualNetworkNumber-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Legt die IPX-Nummer (Internetworking Packet Exchange) des virtuellen Netzwerks auf dem Zielcomputersystem fest. Windows 2000 und Windows NT 3.51 oder höher verwendet eine interne Netzwerknummer für das interne Routing. Die interne Netzwerknummer wird auch als virtuelle Netzwerknummer bezeichnet. Es identifiziert das Computersystem im Netzwerk eindeutig. Die -Methode gibt einen ganzzahligen Wert zurück, der wie folgt interpretiert werden kann:

## <a name="syntax"></a>Syntax


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPXVirtualNetNumber* \[ In\]
</dt> <dd>

Die Nummer des virtuellen Netzwerks für dieses System.

</dd> </dl>

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




