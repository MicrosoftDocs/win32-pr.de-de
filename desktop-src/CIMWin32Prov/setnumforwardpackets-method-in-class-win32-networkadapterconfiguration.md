---
description: Mit der statischen WMI-Klasse SetNumForwardPackets wird die Anzahl der IP-Paketheader festgelegt, die der Routerpaketwarteschlange zugeordnet sind. Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: SetNumForwardPackets-Methode der Win32_NetworkAdapterConfiguration Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1962746cffb64733d6935bb4ef655a96cce051cc67fb1a4f2e730e4ff5ce0d7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759750"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a>SetNumForwardPackets-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Mit der statischen [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **SetNumForwardPackets** wird die Anzahl der IP-Paketheader festgelegt, die der Routerpaketwarteschlange zugeordnet sind. Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumForwardPackets* \[ In\]
</dt> <dd>

Anzahl der IP-Paketheader, die der Routerpaketwarteschlange zugeordnet sind. Dieser Wert sollte mindestens so groß sein wie der Wert der [**ForwardBufferMemory-Eigenschaft**](win32-networkadapterconfiguration.md) dividiert durch die maximale IP-Datengröße der netzwerke, die mit dem Router verbunden sind. Er sollte nicht größer als der **ForwardBufferMemory-Wert** dividiert durch 256 sein, da für jedes Paket mindestens 256 Bytes Vorwärtspufferspeicher erforderlich sind. Die optimale Anzahl von Forward-Paketen für eine bestimmte **ForwardBufferMemory-Größe** hängt von der Art des datenverkehrs im Netzwerk ab und liegt zwischen diesen beiden Werten. Wenn der Router deaktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet. Gültiger Bereich: 1 – 0xFFFFFFFE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und eine andere Zahl, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

DHCP-Dienst kann nicht konfiguriert werden.

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

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="examples"></a>Beispiele

Im VbScript-Beispiel Modify the Number of Allowed Forward Packets (Ändern [der Anzahl zulässiger Weiterleitungspakete)](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) wird die Anzahl der Weiterleitungspakete konfiguriert, die der Routerpaketwarteschlange zugeordnet sind.

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

 

