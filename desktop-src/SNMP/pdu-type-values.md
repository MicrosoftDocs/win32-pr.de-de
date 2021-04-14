---
title: PDU-Typwerte (SNMP. h)
description: Die PDU-Typwerte werden im PDU- \_ type-Feld des PDU verwendet, um den Typ zu beschreiben.
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
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478432"
---
# <a name="pdu-type-values"></a>PDU-Typwerte

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die PDU-Typwerte werden im **PDU- \_ Type** -Feld des PDU verwendet, um den Typ zu beschreiben.



| Konstante                                                                                                                                                                   | BESCHREIBUNG                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**SNMP \_ PDU \_ Get**</dt> </dl>                | Suchen und Abrufen eines Werts aus einer angegebenen SNMP-Variablen.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP \_ PDU \_ GetNext**</dt> </dl>    | Suchen und rufen Sie den Wert einer SNMP-Variablen ab, ohne den genauen Namen der Variablen zu kennen.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**SNMP- \_ PDU- \_ Antwort**</dt> </dl> | Antworten Sie auf eine SNMP \_ PDU \_ Get-oder SNMP \_ PDU \_ GetNext-Anforderung.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**SNMP- \_ PDU- \_ Satz**</dt> </dl>                | Speichert einen Wert in einer angegebenen SNMP-Variablen.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**SNMP \_ PDU \_ V1TRAP**</dt> </dl>       | Gibt an, dass die PDU-Trap so formatiert ist, dass Sie dem SNMPv1-Standard entspricht.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ Getbulk**</dt> </dl>    | Durchsuchen und Abrufen mehrerer Werte mit einer einzelnen Anforderung.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**SNMP \_ PDU- \_ Information**</dt> </dl>       | Gibt eine anforderungsanforderungs-PDU an.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**SNMP- \_ PDU- \_ Trap**</dt> </dl>             | Benachrichtigt das Verwaltungssystem auf ein außergewöhnliches Ereignis unter SNMPv2C.<br/>                             |



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

 

