---
description: SetGateways &\# 32; Die WMI-Klassenmethode gibt eine Liste von Gateways zum Weiterleiten von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: SetGateways-Methode der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 190076822a181d7b0731cb1e7b42eb0cd9d35e37c64aa0736245d1e58994763b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759720"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>SetGateways-Methode der Win32 \_ NetworkAdapterConfiguration-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** gibt eine Liste von Gateways zum Weiterleiten von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefaultIPGateway* \[ In\]
</dt> <dd>

Liste der IP-Adressen für Gateways, an die Netzwerkpakete weitergeleitet werden.

</dd> <dt>

*GatewayCostMetric* \[ in, optional\]
</dt> <dd>

Weist einen Wert zwischen 1 und 9999 zu, der zum Berechnen der schnellsten und zuverlässigsten Routen verwendet wird. Die Werte dieses Parameters entsprechen den Werten im *DefaultIPGateway-Parameter.* Der Standardwert für ein Gateway ist 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und einen beliebigen anderen Wert, wenn ein Fehler auftritt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Erfolgreicher Abschluss, kein Neustart erforderlich**
</dt> <dd>

0

</dd> <dt>

**Erfolgreicher Abschluss, Neustart erforderlich**
</dt> <dd>

1

</dd> <dt>

**Die Methode wird auf dieser Plattform nicht unterstützt.**
</dt> <dd>

64

Die Methode wird nicht unterstützt, wenn sich die NIC im DHCP-Modus befindet.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

65

</dd> <dt>

**Ungültige Subnetzmaske**
</dt> <dd>

66

</dd> <dt>

**Fehler beim Verarbeiten einer zurückgegebenen Instanz**
</dt> <dd>

67

</dd> <dt>

**Ungültiger Eingabeparameter**
</dt> <dd>

68

</dd> <dt>

**Mehr als 5 Gateways angegeben**
</dt> <dd>

69

</dd> <dt>

**Ungültige IP-Adresse**
</dt> <dd>

70

</dd> <dt>

**Ungültige Gateway-IP-Adresse**
</dt> <dd>

71

</dd> <dt>

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen**
</dt> <dd>

72

</dd> <dt>

**Ungültiger Domänenname**
</dt> <dd>

73

</dd> <dt>

**Ungültiger Hostname**
</dt> <dd>

74

</dd> <dt>

**Kein primärer/sekundärer WINS-Server definiert**
</dt> <dd>

75

</dd> <dt>

**Ungültige Datei**
</dt> <dd>

76

</dd> <dt>

**Ungültiger Systempfad**
</dt> <dd>

77

</dd> <dt>

**Fehler beim Kopieren der Datei**
</dt> <dd>

78

</dd> <dt>

**Ungültiger Sicherheitsparameter**
</dt> <dd>

79

</dd> <dt>

**TCP/IP-Dienst kann nicht konfiguriert werden**
</dt> <dd>

80

</dd> <dt>

**DHCP-Dienst kann nicht konfiguriert werden**
</dt> <dd>

81

</dd> <dt>

**DHCP-Lease kann nicht erneuert werden**
</dt> <dd>

82

</dd> <dt>

**DHCP-Lease kann nicht veröffentlicht werden**
</dt> <dd>

83

</dd> <dt>

**IP auf Adapter nicht aktiviert**
</dt> <dd>

84

</dd> <dt>

**IPX auf Adapter nicht aktiviert**
</dt> <dd>

85

</dd> <dt>

**Frame-/Netzwerknummern-Begrenzungsfehler**
</dt> <dd>

86

</dd> <dt>

**Ungültiger Frametyp**
</dt> <dd>

87

</dd> <dt>

**Ungültige Netzwerknummer**
</dt> <dd>

88

</dd> <dt>

**Doppelte Netzwerknummer**
</dt> <dd>

89

</dd> <dt>

**Parameter außerhalb der Grenzen**
</dt> <dd>

90

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

91

</dd> <dt>

**Nicht genügend Arbeitsspeicher.**
</dt> <dd>

92

</dd> <dt>

**Bereits vorhanden**
</dt> <dd>

93

</dd> <dt>

**Pfad, Datei oder Objekt nicht gefunden**
</dt> <dd>

94

</dd> <dt>

**Dienst kann nicht benachrichtigt werden**
</dt> <dd>

95

</dd> <dt>

**DNS-Dienst kann nicht benachrichtigt werden**
</dt> <dd>

96

</dd> <dt>

**Schnittstelle nicht konfigurierbar**
</dt> <dd>

97

</dd> <dt>

**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden.**
</dt> <dd>

98

</dd> <dt>

**DHCP für Adapter nicht aktiviert**
</dt> <dd>

100

</dd> <dt>

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode funktioniert nur, wenn sich die Netzwerkschnittstellenkarte (Network Interface Card, NIC) im statischen IP-Modus befindet.

Um das Gateway zu löschen, legen Sie ihr Gateway auf dieselbe IP-Adresse fest, die Sie unter [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)verwenden.

## <a name="examples"></a>Beispiele

Im VBScript-Beispiel Ändern der [Gateways für](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) einen Netzwerkadapter werden zwei Gateways für einen Netzwerkadapter konfiguriert.

Im [VbScript-Beispiel](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) Zuweisen einer statischen IP-Adresse werden die IP-Adresse und das Gateway eines Computers bestimmt.

Das [PowerShell-Beispiel](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) statische IP und anschließender Beitritt zu einer Domäne hilft bei der Neuerstellung von Computern.

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

 

