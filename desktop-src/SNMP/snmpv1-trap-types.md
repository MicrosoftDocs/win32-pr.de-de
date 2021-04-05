---
title: SNMPv1 Trap-Typen (SNMP. h)
description: Die SNMPv1 Trap-Typen beschreiben einen vordefinierten Satz generischer Trap-Typen, die so formatiert sind, dass Sie dem SNMPv1 Trap-PDU-Standard entsprechen.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859271"
---
# <a name="snmpv1-trap-types"></a>SNMPv1 Trap-Typen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die SNMPv1 Trap-Typen beschreiben einen vordefinierten Satz generischer Trap-Typen, die so formatiert sind, dass Sie dem SNMPv1 Trap-PDU-Standard entsprechen.



| Konstante                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP- \_ generictrap ( \_ coldStart)**</dt> </dl>             | Gibt einen Kaltstart-Trap an. Der Agent initialisiert Protokoll Entitäten im verwalteten Modus. Sie kann Objekte in der Ansicht ändern.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP- \_ generictrap- \_ Warmstart**</dt> </dl>             | Gibt einen warmen Start Trap an. Der Agent wird erneut initialisiert, die Objekte in der Ansicht werden jedoch nicht geändert.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP- \_ generictrap- \_ Link**</dt> </dl>                | Gibt einen linkdown-Trap an. Eine angefügte Schnittstelle hat sich von oben in den Zustand "nach unten" geändert. Die erste Variable in der Variablen Bindungs Liste identifiziert die-Schnittstelle.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**SNMP- \_ generictrap- \_ Verknüpfung**</dt> </dl>                      | Gibt einen Verbindungs Trap an. Eine angefügte Schnittstelle hat sich von unten nach oben geändert. Die erste Variable in der Variablen Bindungs Liste identifiziert die-Schnittstelle.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP- \_ generictrap- \_ authfailure**</dt> </dl>       | Gibt einen Authentifizierungsfehler Trap an. Eine SNMP-Entität hat eine SNMP-Nachricht gesendet, hat aber fälschlicherweise behauptet, zu einer bekannten Community zu gehören.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP- \_ generictrap- \_ egpnachbarloss**</dt> </dl>    | Gibt den Verlust eines EGP-Nachbar Verlusts an. Ein EGP-Peer hat sich in den Zustand "nach unten" geändert. Die erste Variable in der Variablen Bindungs Liste identifiziert die IP-Adresse des EGP-Peers.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP- \_ generictrap Enterprise- \_ spezifisch**</dt> </dl> | Gibt einen unternehmensspezifischen Trap an. Ein außergewöhnliches Ereignis ist aufgetreten. Er wird im Parameter " *specifictrap* " mit einem unternehmensspezifischen Wert identifiziert.<br/>               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Simple Network Management-Protokoll (SNMP) – Übersicht](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[SNMP-Referenz](snmp-reference.md)
</dt> <dt>

[SNMP-Konstanten](snmp-constants.md)
</dt> </dl>

 

