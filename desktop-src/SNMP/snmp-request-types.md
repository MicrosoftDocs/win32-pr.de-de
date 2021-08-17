---
title: SNMP-Anforderungstypen (Snmp.h)
description: Die SNMP-Anforderungstypen werden verwendet, um den Vorgang zu beschreiben, den der SNMP-Dienst vom Erweiterungs-Agent an fordert.
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
ms.openlocfilehash: 74c4dfdfc6d65e63b8cd00956627eef9e831c46c6979e44634067b1e29defc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142993"
---
# <a name="snmp-request-types"></a>SNMP-Anforderungstypen

\[SNMP ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung,](/windows/desktop/WinRM/portal)bei der es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die SNMP-Anforderungstypen werden verwendet, um den Vorgang zu beschreiben, den der SNMP-Dienst vom Erweiterungs-Agent an fordert.



| Konstante/Wert                                                                                                                                                                                                                                                          | Beschreibung                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ ERWEITERUNG \_ GET**</dt> <dt>SNMP \_ PDU \_ GET</dt> </dl>                       | Ruft den Wert der Werte der angegebenen Variablen ab.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ ERWEITERUNG \_ GET \_ NEXT**</dt> <dt>SNMP \_ PDU \_ GETNEXT</dt> </dl>   | Rufen Sie den Wert oder die Werte des lexikografischen Nachfolgers der angegebenen Variablen ab.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ ERWEITERUNG \_ GET \_ BULK**</dt> <dt>SNMP \_ PDU \_ GETBULK</dt> </dl>   | Suchen sie mehrere Werte mit einer einzelnen Anforderung, und rufen Sie sie ab.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**SNMP \_ EXTENSION \_ SET \_ TEST**</dt> </dl>                                                                           | Überprüfen Sie die Werte der angegebenen Variablen. Dieser Vorgang maximiert die Wahrscheinlichkeit eines erfolgreichen Schreibvorgang während der COMMIT-Anforderung. Weitere Informationen finden Sie unter der [**SnmpExtensionQueryEx-Funktion.**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex)<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ EXTENSION \_ SET \_ COMMIT**</dt> <dt>SNMP \_ PDU \_ SET</dt> </dl> | Schreiben Sie die neuen Werte in die angegebenen Variablen.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**SNMP \_ EXTENSION \_ SET \_ UNDO**</dt> </dl>                                                                           | Setzen Sie die Werte der angegebenen Variablen vor der COMMIT-Anforderung auf ihre Werte zurück.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**BEREINIGUNG DES \_ SNMP-ERWEITERUNGSSETS \_ \_**</dt> </dl>                                                                  | Geben Sie die Ressourcen frei, die in vorherigen Anforderungen und Vorgängen zugeordnet wurden.<br/>                                                                                                                                                                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Simple Network Management-Protokoll (SNMP) – Übersicht](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[SNMP-Referenz](snmp-reference.md)
</dt> <dt>

[SNMP-Konstanten](snmp-constants.md)
</dt> </dl>

 

