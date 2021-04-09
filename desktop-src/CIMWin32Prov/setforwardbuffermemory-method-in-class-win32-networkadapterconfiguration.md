---
description: Die statische Methode SetForwardBufferMemory WMI-Klasse wird verwendet, um anzugeben, wie viel Arbeitsspeicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zugeordnet wird.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: SetForwardBufferMemory-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861319"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a>SetForwardBufferMemory-Methode der Win32 \_ networkadapterconfiguration-Klasse

Die statische Methode **SetForwardBufferMemory** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) wird verwendet, um anzugeben, wie viel Arbeitsspeicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zugeordnet wird.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ForwardBufferMemory* \[ in\]
</dt> <dd>

Größe (in Bytes) der Routerpaketwarteschlange, die zum Speichern von Paketdaten verwendet wird. Der Standardwert ist 74240 (50 1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt für einen erfolgreichen Abschluss einen Wert von 0 (null) zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler vorliegt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

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

**Methode wird auf dieser Plattform nicht unterstützt.**
</dt> <dd>

64

Die Methode wird auf dieser Plattform nicht unterstützt.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

65

Unbekannter Fehler.

</dd> <dt>

**Ungültige Subnetzmaske.**
</dt> <dd>

66

Ungültige Subnetzmaske.

</dd> <dt>

**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**
</dt> <dd>

67

Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.

</dd> <dt>

**Ungültiger Eingabeparameter**
</dt> <dd>

68

Ungültiger Eingabeparameter.

</dd> <dt>

**Es wurden mehr als 5 Gateways angegeben.**
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

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**
</dt> <dd>

72

Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.

</dd> <dt>

**Ungültiger Domänen Name**
</dt> <dd>

73

Ungültiger Domänen Name.

</dd> <dt>

**Ungültiger Hostname**
</dt> <dd>

74

Ungültiger Hostname.

</dd> <dt>

**Kein primärer/sekundärer WINS-Server definiert.**
</dt> <dd>

75

Es wurde kein primärer oder sekundärer WINS-Server

</dd> <dt>

**Ungültige Datei**
</dt> <dd>

76

Ungültige Datei.

</dd> <dt>

**Ungültiger Systempfad.**
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

**Der TCP/IP-Dienst kann nicht konfiguriert werden.**
</dt> <dd>

80

Der TCP/IP-Dienst kann nicht konfiguriert werden.

</dd> <dt>

**DHCP-Dienst kann nicht konfiguriert werden.**
</dt> <dd>

81

Der DHCP-Dienst kann nicht konfiguriert werden.

</dd> <dt>

**DHCP-Lease kann nicht erneuert werden.**
</dt> <dd>

82

Die DHCP-Lease kann nicht erneuert werden.

</dd> <dt>

**DHCP-Lease kann nicht freigegeben werden**
</dt> <dd>

83

DHCP-Lease kann nicht freigegeben werden.

</dd> <dt>

**IP ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

84

Die IP ist auf dem Adapter nicht aktiviert.

</dd> <dt>

**IPX ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

85

IPX ist auf dem Adapter nicht aktiviert.

</dd> <dt>

**Fehler bei Frame/Netzwerk Nummer.**
</dt> <dd>

86

Fehler bei Frame-oder Netzwerk Nummern Begrenzungen.

</dd> <dt>

**Ungültiger Frame-Typ**
</dt> <dd>

87

Ungültiger Rahmentyp.

</dd> <dt>

**Ungültige Netzwerk Nummer**
</dt> <dd>

88

Ungültige Netzwerk Nummer.

</dd> <dt>

**Doppelte Netzwerk Nummer**
</dt> <dd>

89

Doppelte Netzwerk Nummer.

</dd> <dt>

**Parameter außerhalb des gültigen Bereichs**
</dt> <dd>

90

Der Parameter liegt außerhalb des gültigen Bereichs.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

91

Zugriff verweigert.

</dd> <dt>

**Nicht genügend Arbeitsspeicher**
</dt> <dd>

92

Nicht genügend Arbeitsspeicher.

</dd> <dt>

**Ist bereits vorhanden.**
</dt> <dd>

93

Ist bereits vorhanden.

</dd> <dt>

**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**
</dt> <dd>

94

Der Pfad, die Datei oder das Objekt wurde nicht gefunden.

</dd> <dt>

**Der Dienst kann nicht benachrichtigt werden.**
</dt> <dd>

95

Der Dienst kann nicht benachrichtigt werden.

</dd> <dt>

**DNS-Dienst kann nicht benachrichtigt werden.**
</dt> <dd>

96

Der DNS-Dienst kann nicht benachrichtigt werden.

</dd> <dt>

**Schnittstelle nicht konfigurierbar**
</dt> <dd>

97

Schnittstelle nicht konfigurierbar.

</dd> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**
</dt> <dd>

98

Nicht alle DHCP-Leases konnten freigegeben oder erneuert werden.

</dd> <dt>

**DHCP ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

100

DHCP ist auf dem Adapter nicht aktiviert.

</dd> <dt>

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn dieser Pufferbereich ausgefüllt ist, beginnt der Router, Pakete zufällig aus der Warteschlange zu verwerfen.

Der Datenpuffer für die Paket Warteschlange beträgt 256 Bytes, sodass der Wert des *ForwardBufferMemory* -Parameters ein Vielfaches von 256 sein sollte. Mehrere Puffer werden für größere Pakete miteinander verkettet. Der IP-Header für ein Paket wird separat gespeichert. Dieser Parameter wird ignoriert, und es werden keine Puffer zugewiesen, wenn der IP-Router nicht aktiviert ist. Die Puffergröße kann zwischen der Netzwerk-maximalen Übertragungseinheit (MTU) und einem Wert kleiner als 0xffffffff liegen.

## <a name="examples"></a>Beispiele

Im Beispiel [Ändern des Forward-Pufferspeichers für alle Netzwerkadapter](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript wird der vorwärts Puffer Arbeitsspeicher für alle Netzwerkadapter auf einem Computer konfiguriert.

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

 

