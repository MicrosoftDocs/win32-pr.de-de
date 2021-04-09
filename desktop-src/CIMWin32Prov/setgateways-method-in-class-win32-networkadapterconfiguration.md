---
description: Die SetGateways &\# 32; WMI-Klassenmethode gibt eine Liste von Gateways für das Routing von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.
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
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861316"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>SetGateways-Methode der Win32 \_ networkadapterconfiguration-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetGateways** gibt eine Liste von Gateways für das Routing von Paketen an ein Subnetz an, das sich von dem Subnetz unterscheidet, mit dem der Netzwerkadapter verbunden ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefaultIPGateway* \[ in\]
</dt> <dd>

Liste der IP-Adressen für Gateways, an die Netzwerkpakete weitergeleitet werden.

</dd> <dt>

*GatewayCostMetric* \[ in, optional\]
</dt> <dd>

Weist einen Wert zwischen 1 und 9999 zu, der verwendet wird, um die schnellsten und zuverlässigsten Routen zu berechnen. Die Werte dieses Parameters entsprechen den Werten im *DefaultIPGateway* -Parameter. Der Standardwert für ein Gateway ist 1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert von 0 (null) für einen erfolgreichen Abschluss zurück, wenn kein Neustart erforderlich ist, 1 (eins) für einen erfolgreichen Abschluss, wenn ein Neustart erforderlich ist, und ein beliebiger anderer Wert, wenn ein Fehler vorliegt. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss, kein Neustart erforderlich**
</dt> <dd>

0

</dd> <dt>

**Erfolgreicher Abschluss, Neustart erforderlich**
</dt> <dd>

1

</dd> <dt>

**Methode wird auf dieser Plattform nicht unterstützt.**
</dt> <dd>

64

Methode wird nicht unterstützt, wenn sich die NIC im DHCP-Modus befindet.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

65

</dd> <dt>

**Ungültige Subnetzmaske.**
</dt> <dd>

66

</dd> <dt>

**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde.**
</dt> <dd>

67

</dd> <dt>

**Ungültiger Eingabeparameter**
</dt> <dd>

68

</dd> <dt>

**Es wurden mehr als 5 Gateways angegeben.**
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

**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen.**
</dt> <dd>

72

</dd> <dt>

**Ungültiger Domänen Name**
</dt> <dd>

73

</dd> <dt>

**Ungültiger Hostname**
</dt> <dd>

74

</dd> <dt>

**Kein primärer/sekundärer WINS-Server definiert.**
</dt> <dd>

75

</dd> <dt>

**Ungültige Datei**
</dt> <dd>

76

</dd> <dt>

**Ungültiger Systempfad.**
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

**Der TCP/IP-Dienst kann nicht konfiguriert werden.**
</dt> <dd>

80

</dd> <dt>

**DHCP-Dienst kann nicht konfiguriert werden.**
</dt> <dd>

81

</dd> <dt>

**DHCP-Lease kann nicht erneuert werden.**
</dt> <dd>

82

</dd> <dt>

**DHCP-Lease kann nicht freigegeben werden**
</dt> <dd>

83

</dd> <dt>

**IP ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

84

</dd> <dt>

**IPX ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

85

</dd> <dt>

**Fehler bei Frame/Netzwerk Nummer.**
</dt> <dd>

86

</dd> <dt>

**Ungültiger Frame-Typ**
</dt> <dd>

87

</dd> <dt>

**Ungültige Netzwerk Nummer**
</dt> <dd>

88

</dd> <dt>

**Doppelte Netzwerk Nummer**
</dt> <dd>

89

</dd> <dt>

**Parameter außerhalb des gültigen Bereichs**
</dt> <dd>

90

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

91

</dd> <dt>

**Nicht genügend Arbeitsspeicher**
</dt> <dd>

92

</dd> <dt>

**Ist bereits vorhanden.**
</dt> <dd>

93

</dd> <dt>

**Der Pfad, die Datei oder das Objekt wurde nicht gefunden.**
</dt> <dd>

94

</dd> <dt>

**Der Dienst kann nicht benachrichtigt werden.**
</dt> <dd>

95

</dd> <dt>

**DNS-Dienst kann nicht benachrichtigt werden.**
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

**DHCP ist auf dem Adapter nicht aktiviert.**
</dt> <dd>

100

</dd> <dt>

**Andere**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode funktioniert nur, wenn sich die Netzwerkschnittstellenkarte (NIC) im statischen IP-Modus befindet.

Um das Gateway zu löschen, legen Sie das Gateway auf die gleiche IP-Adresse fest, die Sie in [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)verwenden.

## <a name="examples"></a>Beispiele

Im Beispiel [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript werden zwei Gateways für einen Netzwerkadapter konfiguriert.

Im Beispiel [Zuweisen einer statischen IP-Adresse](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) (VBScript) werden die IP-Adresse und das Gateway eines Computers festgelegt.

Die [statische IP-Adresse und die anschließende Verknüpfung mit einem Domänen-](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell-Beispiel unterstützt die Neuerstellung von

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

 

