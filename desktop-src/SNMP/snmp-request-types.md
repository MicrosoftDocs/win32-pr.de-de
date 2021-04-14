---
title: SNMP-Anforderungs Typen (SNMP. h)
description: Die SNMP-Anforderungs Typen werden verwendet, um den Vorgang zu beschreiben, der vom SNMP-Dienst für die Ausführung angefordert wird.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478429"
---
# <a name="snmp-request-types"></a>SNMP-Anforderungs Typen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die SNMP-Anforderungs Typen werden verwendet, um den Vorgang zu beschreiben, der vom SNMP-Dienst für die Ausführung angefordert wird.



| Konstante/Wert                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ Erweiterung \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt> </dl>                       | Ruft den Wert der Werte der angegebenen Variablen ab.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ Erweiterung \_ get \_ Next**</dt> <dt>SNMP \_ PDU \_ GetNext</dt> </dl>   | Ruft den Wert oder die Werte des lexikografischen Nachfolgers der angegebenen Variablen ab.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ Erweiterung \_ get \_ Bulk**</dt> <dt>SNMP \_ PDU \_ Getbulk</dt> </dl>   | Durchsuchen und Abrufen mehrerer Werte mit einer einzelnen Anforderung.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**SNMP- \_ Erweiterungs \_ Satz \_ Test**</dt> </dl>                                                                           | Überprüfen Sie die Werte der angegebenen Variablen. Dieser Vorgang maximiert die Wahrscheinlichkeit eines erfolgreichen Schreibvorgangs während der commitanforderung. Weitere Informationen finden Sie in der Funktion [**snmpextensionqueryex**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ Erweiterungs \_ Satz \_ Commit**</dt> für <dt>SNMP- \_ PDU \_ festgelegt</dt> </dl> | Schreiben Sie die neuen Werte in die angegebenen Variablen.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**SNMP- \_ Erweiterungs \_ Satz \_ rückgängig machen**</dt> </dl>                                                                           | Setzen Sie die Werte der angegebenen Variablen auf ihre Werte vor der Commit-Anforderung zurück.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**Cleanup für SNMP- \_ Erweiterungs \_ Satz \_**</dt> </dl>                                                                  | Geben Sie die in vorherigen Anforderungen und Vorgängen zugeordneten Ressourcen frei.<br/>                                                                                                                                                                             |



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

 

