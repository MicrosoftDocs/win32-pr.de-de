---
description: Die EnableStatic WMI-Klassenmethode aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerkadapter. Daher ist DHCP für diesen Netzwerkadapter deaktiviert.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: EnableStatic-Methode der Win32_NetworkAdapterConfiguration Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03d2c7214f9cfb89b8efcb612f3bc07840448ff0eaf1b064556d2797b74d4822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918420"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a>EnableStatic-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Die **EnableStatic** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerkadapter. Daher ist DHCP für diesen Netzwerkadapter deaktiviert.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IPAddress* \[ In\]
</dt> <dd>

Listet alle statischen IP-Adressen für den aktuellen Netzwerkadapter auf.

Beispiel: 155.34.22.0.

</dd> <dt>

*SubnetMask* \[ In\]
</dt> <dd>

Subnetzmasken, die die Werte im *IPAddress-Parameter* ergänzen.

Beispiel: 255.255.0.0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine beliebige andere Zahl, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

**Methode wird auf dieser Plattform nicht unterstützt**
</dt> <dd>

64

Methode wird auf dieser Plattform nicht unterstützt.

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

**Fehler beim Verarbeiten einer instanz, die zurückgegeben wurde**
</dt> <dd>

67

Fehler beim Verarbeiten einer instanz, die zurückgegeben wurde.

</dd> <dt>

**Ungültiger Eingabeparameter**
</dt> <dd>

68

Ungültiger Eingabeparameter.

</dd> <dt>

**Mehr als fünf Gateways angegeben**
</dt> <dd>

69

Es wurden mehr als fünf Gateways angegeben.

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

**Fehler beim Zugreifen auf die Registrierung für die angeforderten Informationen**
</dt> <dd>

72

Fehler beim Zugreifen auf die Registrierung für die angeforderten Informationen.

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

Kein primärer oder sekundärer WINS-Server definiert.

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

Der TCP/IP-Dienst kann nicht konfiguriert werden.

</dd> <dt>

**DHCP-Dienst kann nicht konfiguriert werden**
</dt> <dd>

81

DHCP-Dienst kann nicht konfiguriert werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

**DHCP-Lease kann nicht verlängert werden**
</dt> <dd>

82

DHCP-Lease kann nicht erneuert werden.

</dd> <dt>

**DHCP-Lease kann nicht veröffentlicht werden**
</dt> <dd>

83

DHCP-Lease kann nicht veröffentlicht werden.

</dd> <dt>

**IP-Adresse auf Adapter nicht aktiviert**
</dt> <dd>

84

DIE IP-Adresse ist auf dem Adapter nicht aktiviert.

</dd> <dt>

**IPX auf Adapter nicht aktiviert**
</dt> <dd>

85

IPX ist auf adapter nicht aktiviert.

</dd> <dt>

**Frame-/Netzwerknummer-Begrenzungsfehler**
</dt> <dd>

86

Frame- oder Netzwerknummer-Begrenzungsfehler.

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

Nicht alle DHCP-Leases können freigegeben oder erneuert werden.

</dd> <dt>

**DHCP für Adapter nicht aktiviert**
</dt> <dd>

100

DHCP für Adapter nicht aktiviert.

</dd> <dt>

**2147786788**
</dt> <dd>

Schreibsperre nicht aktiviert. Weitere Informationen finden Sie unter [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).

</dd> <dt>

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn **Sie EnableStatic** verwenden, um die IP-Adresse des Remotecomputers zu ändern, während sie über diesen Adapter verbunden ist, verlieren Sie wahrscheinlich die Verbindung mit dem Remotecomputer und erhalten eine RPC-Fehlermeldung, die nicht verfügbar ist. (Die Einstellungen werden jedoch geändert.) Um dieses Szenario zu vermeiden, sollten Sie die Gateway- und/oder DNS-Einstellungen ändern, bevor Sie die IP-Adresse des Adapters festlegen.

Wenn **Sie EnableStatic** verwenden, um einem Adapter eine statische IP-Konfiguration zu geben, gibt die Funktion "81 – DHCP-Dienst kann nicht konfiguriert werden" zurück, wenn der Adapter bereits mit einer statischen Adresse konfiguriert ist. Die Funktion kann jedoch weiterhin mit dem neuen Vorgang festgelegt werden.

## <a name="examples"></a>Beispiele

Die [statische IP-Adresse und anschließende Verknüpfung mit einer PowerShell-Domäne](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) im TechNet-Katalog verwendet **EnableStatic,** um einem lokalen Computer eine statische IP-Adresse hinzuzufügen.

Im [VbScript-Codebeispiel Zuweisen einer statischen IP-Adresse](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) im TechNet-Katalog wird **EnableStatic** verwendet, um die IP-Adresse eines Computers festzulegen.

Im folgenden VBScript-Beispiel wird veranschaulicht, wie die DHCP-Verwendung für eine Instanz von [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)deaktiviert wird. In diesem Fall geben wir den Adapter mit dem Index 0 an. Der richtige Index sollte aus Win32 \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.

> [!Note]  
> Dieses Skript gilt nur für NT-basierte Systeme Ändern Sie die unten aufgeführten ipaddr- und Subnetzvariablen in die Werte, die Sie auf den Adapter anwenden möchten.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



Im folgenden Perl-Beispiel wird veranschaulicht, wie die DHCP-Verwendung für eine Instanz von [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)deaktiviert wird. In diesem Fall geben wir den Adapter mit dem Index 0 an. Der richtige Index sollte aus Win32 \_ NetworkAdapter-Instanzen für andere Schnittstellen ausgewählt werden.

> [!Note]  
> Dieses Skript gilt nur für NT-basierte Systeme Ändern Sie die unten aufgeführten ipaddr- und Subnetzvariablen in die Werte, die Sie auf den Adapter anwenden möchten.

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

