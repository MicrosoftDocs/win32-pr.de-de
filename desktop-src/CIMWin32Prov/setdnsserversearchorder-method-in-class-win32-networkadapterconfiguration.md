---
description: SetDNSServerSearchOrder &\# 32; Die WMI-Klassenmethode verwendet ein Array von Zeichen folgen Elementen, um die Server Such Reihenfolge festzulegen.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: SetDNSServerSearchOrder-Methode der Win32_NetworkAdapterConfiguration-Klasse
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
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041472"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>SetDNSServerSearchOrder-Methode der Win32 \_ networkadapterconfiguration-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDNSServerSearchOrder** verwendet ein Array von Zeichen folgen Elementen, um die Server Such Reihenfolge festzulegen.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DNSServerSearchOrder* \[ in\]
</dt> <dd>

Liste der Server-IP-Adressen für die Abfrage von DNS-Servern.

Beispiel: 130.215.24.1 oder 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

**Sonstige** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um einen instanzabhängigen Methoden Aufrufwert, der pro Adapter angewendet wird. Nachdem statische DNS-Server angegeben wurden, um mit der Verwendung des Dynamic Host Configuration-Protokolls (DHCP) anstelle statischer DNS-Server zu beginnen, können Sie die Methode ohne Angabe von "in"-Parametern abrufen.

## <a name="examples"></a>Beispiele

Die [Such Reihenfolge der DNS-Server Suche für mehrere Computer in einer Organisationseinheit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) "VBScript" in der TechNet Gallery Ruft die DNS-Server Such Reihenfolge für mehrere Computer ab, die einer Organisationseinheit angehören, oder legt diese fest

Das Beispiel [Ändern der DNS-Server-Such Reihenfolge für ein Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript konfiguriert einen TCP/IP-gebundenen Netzwerkadapter für die Verwendung von zwei DNS-Servern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[WMI-Tasks: Netzwerk](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[WMI-Tasks: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[IPv6-und IPv4-Unterstützung in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

