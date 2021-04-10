---
title: SNMP-Anwendungs Syntax Werte (SNMP. h)
description: Die SNMP-Anwendungs Syntax Werte werden von Verwaltungs Anwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.
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
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103423"
---
# <a name="snmp-application-syntax-values"></a>SNMP-Anwendungs Syntax Werte

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die SNMP-Anwendungs Syntax Werte werden von Verwaltungs Anwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.



| Konstante                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**ASN- \_ IPAddress**</dt> </dl>                             | Gibt eine IP-Adress Variable an.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**ASN \_ COUNTER32**</dt> </dl>                             | Gibt eine Counter-Variable an.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**ASN \_ GAUGE32**</dt> </dl>                                   | Gibt eine Messgeräte Variable an. Diese Variable beschreibt einen Unsigned32-Typ in Übereinstimmung mit RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**ASN- \_ TimeTicks**</dt> </dl>                             | Gibt eine TimeTicks-Variable an.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN \_ nicht transparent**</dt> </dl>                                      | Gibt eine nicht transparente Variable an.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**ASN \_ COUNTER64**</dt> </dl>                             | Gibt eine-Counter-Variable an, die zunimmt, bis Sie den maximalen Wert erreicht (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**ASN \_ UINTEGER32**</dt> </dl>                          | Gibt eine 32-Bit-Ganzzahl ohne Vorzeichen an. Diese Variable beschreibt einen UInteger32-Typ in Übereinstimmung mit RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | Siehe ASN \_ GAUGE32.<br/>                                                                                                     |



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

 

