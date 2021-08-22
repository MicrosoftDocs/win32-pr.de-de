---
title: PDU-Typwerte (Snmp.h)
description: Die PDU-Typwerte werden im \_ PDU-Typfeld der PDU verwendet, um ihren Typ zu beschreiben.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e9346c313efccda6d3635da51919f52fae37dd901cc73cf1f119bffdf9c22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009208"
---
# <a name="pdu-type-values"></a>PDU-Typwerte

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die PDU-Typwerte werden im **PDU-Typfeld \_** der PDU verwendet, um ihren Typ zu beschreiben.



| Konstante                                                                                                                                                                   | BESCHREIBUNG                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**SNMP \_ PDU \_ GET**</dt> </dl>                | Suchen Sie nach einem Wert, und rufen Sie einen Wert aus einer angegebenen SNMP-Variablen ab.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP \_ PDU \_ GETNEXT**</dt> </dl>    | Suchen Sie den Wert einer SNMP-Variablen, und rufen Sie sie ab, ohne den genauen Namen der Variablen zu kennen.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**\_SNMP-PDU-ANTWORT \_**</dt> </dl> | Antwort auf eine \_ SNMP-PDU \_ GET- oder SNMP-PDU \_ \_ GETNEXT-Anforderung.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_SNMP-PDU-SET \_**</dt> </dl>                | Store einen Wert in einer angegebenen SNMP-Variablen.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**SNMP \_ PDU \_ V1TRAP**</dt> </dl>       | Gibt an, dass der PDU-Trap so formatiert ist, dass er dem SNMPv1-Standard entspricht.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GETBULK**</dt> </dl>    | Suchen sie mehrere Werte, und rufen Sie sie mit einer einzelnen Anforderung ab.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**SNMP \_ PDU \_ INFORM**</dt> </dl>       | Gibt eine Informationsanforderungs-PDU an.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**\_SNMP-PDU-TRAP \_**</dt> </dl>             | Benachrichtigt das Verwaltungssystem unter SNMPv2C über ein ereignisereignisses Ereignis.<br/>                             |



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

 

