---
description: Die statische WMI-Klasse SetDNSSuffixSearchOrder verwendet ein Array von Zeichenfolgenelementen, um die Suffixsuchreihenfolge festzulegen.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: SetDNSSuffixSearchOrder-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85964d24c82367c8609e4f93b02f5614493c56efa299386038d7f73fd749dcab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440040"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>SetDNSSuffixSearchOrder-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Die statische **WMI-Klasse SetDNSSuffixSearchOrder** [](/windows/desktop/WmiSdk/retrieving-a-class) verwendet ein Array von Zeichenfolgenelementen, um die Suffixsuchreihenfolge festzulegen.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DNSDomainSuffixSearchOrder* \[ In\]
</dt> <dd>

Liste der Serversuffixe, die nach DNS-Servern abgefragt werden sollen. Der Registrierungsspeicherort des DNS-Suffixes lautet **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tcpip \| NameServer.**

Beispiel: "suffix1.company.com", "suffix2.company.com"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolgreicher Abschluss, kein Neustart erforderlich**
</dt> <dd>

0

Erfolgreicher Abschluss, kein Neustart erforderlich.

</dd> <dt>

**Erfolgreicher Abschluss, Neustart erforderlich**
</dt> <dd>

1

Erfolgreicher Abschluss, Neustart erforderlich.

</dd> <dt>

**Die Methode wird auf dieser Plattform nicht unterstützt.**
</dt> <dd>

64

Die Methode wird auf dieser Plattform nicht unterstützt.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

65

Unbekannter Fehler.

</dd> <dt>

**Ungültige Subnetzmaske**
</dt> <dd>

66

Ungültige Subnetzmaske.

</dd> <dt>

**Fehler beim Verarbeiten einer zurückgegebenen Instanz**
</dt> <dd>

67

Fehler beim Verarbeiten einer zurückgegebenen Instanz.

</dd> <dt>

**Ungültiger Eingabeparameter**
</dt> <dd>

68

Ungültiger Eingabeparameter.

</dd> <dt>

**Mehr als 5 Gateways angegeben**
</dt> <dd>

69

Mehr als fünf Gateways angegeben.

</dd> <dt>

**Ungültige IP-Adresse**
</dt> <dd>

70

Ungültige IP-Adresse.

</dd> <dt>

**Ungültige Gateway-IP-Adresse**
</dt> <dd>

71

Ungültige Gateway-IP-Adresse.

</dd> <dt>

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen**
</dt> <dd>

72

Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.

</dd> <dt>

**Ungültiger Domänenname**
</dt> <dd>

73

Ungültiger Domänenname.

</dd> <dt>

**Ungültiger Hostname**
</dt> <dd>

74

Ungültiger Hostname.

</dd> <dt>

**Kein primärer/sekundärer WINS-Server definiert**
</dt> <dd>

75

Es wurde kein primärer oder sekundärer WINS-Server definiert.

</dd> <dt>

**Ungültige Datei**
</dt> <dd>

76

Ungültige Datei.

</dd> <dt>

**Ungültiger Systempfad**
</dt> <dd>

77

Ungültiger Systempfad.

</dd> <dt>

**Fehler beim Kopieren der Datei**
</dt> <dd>

78

Fehler beim Kopieren der Datei.

</dd> <dt>

**Ungültiger Sicherheitsparameter**
</dt> <dd>

79

Ungültiger Sicherheitsparameter.

</dd> <dt>

**TCP/IP-Dienst kann nicht konfiguriert werden**
</dt> <dd>

80

Tcp/IP-Dienst kann nicht konfiguriert werden.

</dd> <dt>

**DHCP-Dienst kann nicht konfiguriert werden**
</dt> <dd>

81

Dhcp-Dienst kann nicht konfiguriert werden.

</dd> <dt>

**DHCP-Lease kann nicht erneuert werden**
</dt> <dd>

82

DHCP-Lease kann nicht erneuert werden.

</dd> <dt>

**DHCP-Lease kann nicht veröffentlicht werden**
</dt> <dd>

83

DHCP-Lease kann nicht veröffentlicht werden.

</dd> <dt>

**IP auf Adapter nicht aktiviert**
</dt> <dd>

84

DIE IP-Adresse ist auf dem Adapter nicht aktiviert.

</dd> <dt>

**IPX auf Adapter nicht aktiviert**
</dt> <dd>

85

IPX für Adapter nicht aktiviert.

</dd> <dt>

**Frame-/Netzwerknummern-Begrenzungsfehler**
</dt> <dd>

86

Frame- oder Netzwerknummern-Begrenzungsfehler.

</dd> <dt>

**Ungültiger Frametyp**
</dt> <dd>

87

Ungültiger Frametyp.

</dd> <dt>

**Ungültige Netzwerknummer**
</dt> <dd>

88

Ungültige Netzwerknummer.

</dd> <dt>

**Doppelte Netzwerknummer**
</dt> <dd>

89

Doppelte Netzwerknummer.

</dd> <dt>

**Parameter außerhalb der Grenzen**
</dt> <dd>

90

Parameter außerhalb der Grenzen.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

91

Zugriff verweigert:

</dd> <dt>

**Nicht genügend Arbeitsspeicher.**
</dt> <dd>

92

Nicht genügend Arbeitsspeicher.

</dd> <dt>

**Bereits vorhanden**
</dt> <dd>

93

Ist bereits vorhanden.

</dd> <dt>

**Pfad, Datei oder Objekt nicht gefunden**
</dt> <dd>

94

Pfad, Datei oder Objekt nicht gefunden.

</dd> <dt>

**Dienst kann nicht benachrichtigt werden**
</dt> <dd>

95

Der Dienst kann nicht benachrichtigt werden.

</dd> <dt>

**DNS-Dienst kann nicht benachrichtigt werden**
</dt> <dd>

96

Der DNS-Dienst kann nicht benachrichtigt werden.

</dd> <dt>

**Schnittstelle nicht konfigurierbar**
</dt> <dd>

97

Die Schnittstelle kann nicht konfiguriert werden.

</dd> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**
</dt> <dd>

98

Nicht alle DHCP-Leases werden freigegeben oder erneuert.

</dd> <dt>

**DHCP für Adapter nicht aktiviert**
</dt> <dd>

100

DHCP für Adapter nicht aktiviert.

</dd> <dt>

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dies ist ein instanzunabhängiger Aufruf, der für alle Adapter gilt, jedoch nur für Windows.

## <a name="examples"></a>Beispiele

Im VBScript-Codebeispiel Modify the DNS Suffix Search Order for All Network Adapters (ÄNDERN [der DNS-Suffixsuchreihenfolge für alle Netzwerkadapter)](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) wird ein Computer so konfiguriert, dass beim Ausführen von DNS-Suchen zwei DNS-Suffixe verwendet werden.

Im Beispiel [DHCP Einstellungen auf einem Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) vbScript aktivieren werden alle Einstellungen konfiguriert, die normalerweise zum Aktivieren von DHCP auf einem Computer erforderlich sind.

Der folgende PowerShell-Code legt die Dns-Suffixsuchreihenfolge fest.


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



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

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[WMI-Aufgaben: Netzwerk](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[WMI-Aufgaben: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[IPv6- und IPv4-Unterstützung in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

