---
title: Syntaxwerte der SNMP-Anwendung (Snmp.h)
description: Die Syntaxwerte der SNMP-Anwendung werden von Verwaltungsanwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009028"
---
# <a name="snmp-application-syntax-values"></a>Syntaxwerte der SNMP-Anwendung

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung,](/windows/desktop/WinRM/portal)bei der es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die Syntaxwerte der SNMP-Anwendung werden von Verwaltungsanwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.



| Konstante                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**ASN \_ IPADDRESS**</dt> </dl>                             | Gibt eine IP-Adressvariable an.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**ASN \_ COUNTER32**</dt> </dl>                             | Gibt eine Indikatorvariable an.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**ASN \_ GAUGE32**</dt> </dl>                                   | Gibt eine Messgerätvariable an. Diese Variable beschreibt einen Unsigned32-Typ in Übereinstimmung mit RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**ASN \_ TIMETICKS**</dt> </dl>                             | Gibt eine Timeticks-Variable an.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ NICHT TRANSPARENT**</dt> </dl>                                      | Gibt eine nicht transparente Variable an.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**ASN \_ COUNTER64**</dt> </dl>                             | Gibt eine Indikatorvariable an, die erhöht wird, bis sie den Maximalwert (2^64) – 1 erreicht.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**ASN \_ UINTEGER32**</dt> </dl>                          | Gibt eine 32-Bit-Ganzzahlvariable ohne Vorzeichen an. Diese Variable beschreibt einen UInteger32-Typ in Übereinstimmung mit RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | Siehe ASN \_ GAUGE32.<br/>                                                                                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Simple Network Management-Protokoll (SNMP) – Übersicht](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[SNMP-Referenz](snmp-reference.md)
</dt> <dt>

[SNMP-Konstanten](snmp-constants.md)
</dt> </dl>

 

