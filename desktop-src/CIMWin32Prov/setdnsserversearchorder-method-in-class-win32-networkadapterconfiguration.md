---
description: SetDNSServerSearchOrder &\# 32; Die WMI-Klassenmethode verwendet ein Array von Zeichenfolgenelementen zum Festlegen der Serversuch reihenfolge.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: SetDNSServerSearchOrder-Methode der Win32_NetworkAdapterConfiguration Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ae53996e2f8199d552909a186ab17e6b7ec89857c9be24dc4d8d4bfe583cfea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759800"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>SetDNSServerSearchOrder-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Die **WMI-Klassenmethode SetDNSServerSearchOrder** [](/windows/desktop/WmiSdk/retrieving-a-class) verwendet ein Array von Zeichenfolgenelementen, um die Serversuch reihenfolge fest zu legen.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DNSServerSearchOrder* \[ In\]
</dt> <dd>

Liste der Server-IP-Adressen, die für DNS-Server abfragen werden.

Beispiel: 130.215.24.1 oder 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

**Fehler beim Verarbeiten einer instanz, die zurückgegeben wurde** (67)
</dt> <dt>

**Ungültiger Eingabeparameter** (68)
</dt> <dt>

**Mehr als 5 Gateways angegeben** (69)
</dt> <dt>

**Ungültige IP-Adresse** (70)
</dt> <dt>

**Ungültige Gateway-IP-Adresse** (71)
</dt> <dt>

**Fehler beim Zugreifen auf die Registrierung für die angeforderten Informationen** (72)
</dt> <dt>

**Ungültiger Domänenname** (73)
</dt> <dt>

**Ungültiger Hostname** (74)
</dt> <dt>

**Kein primärer/sekundärer WINS-Server definiert** (75)
</dt> <dt>

**Ungültige** Datei (76)
</dt> <dt>

**Ungültiger Systempfad** (77)
</dt> <dt>

**Fehler beim Kopieren der** Datei (78)
</dt> <dt>

**Ungültiger Sicherheitsparameter** (79)
</dt> <dt>

**TCP/IP-Dienst kann nicht konfiguriert werden** (80)
</dt> <dt>

**DHCP-Dienst kann nicht konfiguriert werden** (81)
</dt> <dt>

**DHCP-Lease kann nicht erneuert werden** (82)
</dt> <dt>

**DHCP-Lease kann nicht veröffentlicht werden** (83)
</dt> <dt>

**IP-Adresse auf Adapter nicht aktiviert** (84)
</dt> <dt>

**IPX auf Adapter nicht aktiviert** (85)
</dt> <dt>

**Frame-/Netzwerknummer-Begrenzungsfehler** (86)
</dt> <dt>

**Ungültiger Frametyp** (87)
</dt> <dt>

**Ungültige Netzwerknummer** (88)
</dt> <dt>

**Doppelte Netzwerknummer** (89)
</dt> <dt>

**Parameter out-of-bounds** (90)
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

**Dns-Dienst kann nicht benachrichtigt werden** (96)
</dt> <dt>

**Schnittstelle nicht konfigurierbar** (97)
</dt> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98)
</dt> <dt>

**DHCP auf Adapter nicht aktiviert** (100)
</dt> <dt>

**Andere** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Dies ist ein instanzabhängiger Methodenaufruf, der pro Adapter gilt. Nachdem statische DNS-Server angegeben wurden, um mit der Verwendung des Dynamic Host Configuration-Protokolls (DHCP) anstelle von statischen DNS-Servern zu beginnen, können Sie die -Methode aufrufen, ohne "in"-Parameter anzugeben.

## <a name="examples"></a>Beispiele

Im VbScript-Beispiel Set [DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) (DNS-Serversuch reihenfolge für mehrere Computer in einer Organisationseinheit) im TechNet-Katalog wird die DNS-Serversuch reihenfolge für mehrere Computer abgerufen oder festgelegt, die zu einer Organisationseinheit gehören.

Im VbScript-Beispiel Ändern der [DNS-Serversuch](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) reihenfolge für einen Netzwerkadapter wird ein TCP/IP-gebundener Netzwerkadapter für die Verwendung von zwei DNS-Servern konfiguriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[WMI-Aufgaben: Netzwerk](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[WMI-Aufgaben: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[IPv6- und IPv4-Unterstützung in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

