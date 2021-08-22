---
description: EnableWINS &\# 32; Die statische WMI-Klasse ermöglicht Windows INTERNET NAMING SERVICE (WINS)-Einstellungen für TCP/IP, jedoch unabhängig vom Netzwerkadapter.
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
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676503"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>EnableWINS-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Die **statische Methode der EnableWINS** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) ermöglicht Windows INTERNET NAMING SERVICE(WINS)-Einstellungen für TCP/IP, jedoch unabhängig vom Netzwerkadapter.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*DNSEnabledForWINSResolution* \[ In\]
</dt> <dd>

True **gibt an,** dass Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung aktiviert ist.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ In\]
</dt> <dd>

True **gibt an,** dass lokale Nachschlagedateien verwendet werden. Suchdateien enthalten Zuordnungen von IP-Adressen zu Hostnamen.

</dd> <dt>

*WINSHostLookupFile* \[ in, optional\]
</dt> <dd>

Nachschlagedateien, die Zuordnungen von IP-Adressen zu Hostnamen enthalten. Falls verfügbar, finden Sie die Dateien unter %SystemRoot% \\ system32 drivers (%SystemRoot%-System32-Treiber). \\ \\

</dd> <dt>

*WINSScopeID* \[ in, optional\]
</dt> <dd>

Der Wert des Bereichsbezeichners, der an das Ende des NetBIOS-Namens des Computers angefügt wird. Systeme, die denselben Bereichsbezeichner verwenden, können mit diesem Computer kommunizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist. 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist; eine andere Zahl, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

**IP-Adresse für Adapter nicht aktiviert** (84)
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

## <a name="examples"></a>Beispiele

Im VBScript-Codebeispiel ENABLE [WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) (WINS für alle Netzwerkadapter aktivieren) im TechNet-Katalog wird **EnableWINS** verwendet, um WINS auf allen auf einem Computer installierten Netzwerkadaptern zu aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

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

 

