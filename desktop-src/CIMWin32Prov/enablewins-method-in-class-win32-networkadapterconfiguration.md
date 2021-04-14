---
description: Die EnableWINS-&\# 32; Die statische WMI-Klassenmethode aktiviert Windows Internet Naming Service (WINS)-Einstellungen für TCP/IP, aber unabhängig vom Netzwerkadapter.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: EnableWINS-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523387"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>EnableWINS-Methode der Win32 \_ networkadapterconfiguration-Klasse

Mit der statischen Methode " **EnableWINS** " der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) können Windows Internet Naming Service (WINS)-Einstellungen speziell für TCP/IP, aber unabhängig vom Netzwerkadapter aktiviert werden.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DNSEnabledForWINSResolution* \[ in\]
</dt> <dd>

**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung aktiviert ist.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ in\]
</dt> <dd>

**True** gibt an, dass lokale Suchdateien verwendet werden. Suchdateien enthalten Zuordnungen von IP-Adressen zu Hostnamen.

</dd> <dt>

*WINSHostLookupFile* \[ in, optional\]
</dt> <dd>

Suchdateien, die Zuordnungen von IP-Adressen zu Hostnamen enthalten. Wenn Sie verfügbar sind, befinden sich die Dateien unter% systemroot% \\ system32 \\ Drivers \\ .

</dd> <dt>

*WINSScopeID* \[ in, optional\]
</dt> <dd>

Der Wert des Bereichs Bezeichners, der am Ende des NetBIOS-Namens des Computers angefügt wird. Systeme, die denselben Bereichs Bezeichner verwenden, können mit diesem Computer kommunizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist. 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist. eine andere Zahl, wenn ein Fehler vorliegt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Beispiele

Das Codebeispiel [Aktivieren von WINS für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript in der TechNet Gallery verwendet **EnableWINS** , um WINS auf allen Netzwerkadaptern zu aktivieren, die auf einem Computer installiert sind.

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

 

