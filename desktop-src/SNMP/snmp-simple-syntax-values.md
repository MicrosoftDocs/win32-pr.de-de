---
title: Einfache SNMP-Syntax Werte (SNMP. h)
description: Die einfachen SNMP-Syntax Werte werden verwendet, um einen SNMP-Variablentyp anzugeben.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104373"
---
# <a name="snmp-simple-syntax-values"></a>Einfache SNMP-Syntax Werte

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die einfachen SNMP-Syntax Werte werden verwendet, um einen SNMP-Variablentyp anzugeben.



| Konstante                                                                                                                                                                           | BESCHREIBUNG                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**ASN- \_ Ganzzahl**</dt> </dl>                            | Gibt eine 32-Bit-Ganzzahl mit Vorzeichen an.<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**ASN- \_ Bits**</dt> </dl>                                     | Gibt eine Variable an, die eine Enumeration benannter Bits ist.<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**ASN \_ octetstring**</dt> </dl>                | Gibt eine Oktett-Zeichen folgen Variable an.<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**ASN \_ null**</dt> </dl>                                     | Gibt einen **null** -Wert an.<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**ASN- \_ objectidentifier**</dt> </dl> | Gibt eine objektbezeichnervariable an.<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**ASN \_ INTEGER32**</dt> </dl>                      | Gibt einen 32-Bit-Ganzzahl mit Vorzeichen an.<br/>                   |



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

 

