---
title: SNMP-Fehlercodes (Snmp.h)
description: Microsoft implementiert die folgenden SNMP-Fehlercodes, die durch die SNMPv2C-Spezifikation definiert werden.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583394dfc3093f4f0d5cf3d7c7cef68d7ff6d57930e3abf957d857defec227c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008928"
---
# <a name="snmp-error-codes"></a>SNMP-Fehlercodes

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung,](/windows/desktop/WinRM/portal)bei der es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Microsoft implementiert die folgenden SNMP-Fehlercodes, die durch die SNMPv2C-Spezifikation definiert werden.



| Konstante/Wert                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOERROR**</dt> <dt>0</dt> </dl>                                      | Der Agent meldet, dass während der Übertragung keine Fehler aufgetreten sind.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | Der Agent konnte die Ergebnisse des angeforderten SNMP-Vorgangs nicht in einer einzelnen SNMP-Nachricht platzieren.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt> </dl>                             | Der angeforderte SNMP-Vorgang hat eine unbekannte Variable identifiziert.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | Der angeforderte SNMP-Vorgang hat versucht, eine Variable zu ändern, aber es wurde entweder ein Syntax- oder Wertfehler angegeben.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ READONLY**</dt> <dt>4</dt> </dl>                                   | Der angeforderte SNMP-Vorgang hat versucht, eine Variable zu ändern, die gemäß dem Communityprofil der Variablen nicht geändert werden konnte.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ GENERR**</dt> <dt>5</dt> </dl>                                         | Während des angeforderten SNMP-Vorgangs ist ein anderer Fehler als einer der hier aufgeführten aufgetreten.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOACCESS**</dt> <dt>6</dt> </dl>                                   | Auf die angegebene SNMP-Variable kann nicht zugegriffen werden.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt> </dl>                                | Der -Wert gibt einen Typ an, der mit dem für die Variable erforderlichen Typ inkonsistent ist.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | Der -Wert gibt eine Länge an, die mit der für die Variable erforderlichen Länge inkonsistent ist.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | Der Wert enthält eine ASN.1-Codierung (Abstract Syntax Notation One), die mit dem ASN.1-Tag des Felds inkonsistent ist.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGVALUE**</dt> <dt>10</dt> </dl>                            | Der Wert kann der Variablen nicht zugewiesen werden.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOCREATION**</dt> <dt>11</dt> </dl>                            | Die Variable ist nicht vorhanden, und der Agent kann sie nicht erstellen.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt> </dl>       | Der Wert ist inkonsistent mit den Werten anderer verwalteter Objekte.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | Das Zuweisen des Werts zur Variablen erfordert die Zuordnung von Ressourcen, die derzeit nicht verfügbar sind.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | Es sind keine Validierungsfehler aufgetreten, aber es wurden keine Variablen aktualisiert.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt> </dl>                            | Es sind keine Validierungsfehler aufgetreten. Einige Variablen wurden aktualisiert, da es nicht möglich war, ihre Zuweisung rückgängig zu machen.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Ein Autorisierungsfehler ist aufgetreten.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt> </dl>                         | Die Variable ist vorhanden, aber der Agent kann sie nicht ändern.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt> </dl>          | Die Variable ist nicht vorhanden. Der Agent kann sie nicht erstellen, da die benannte Objektinstanz mit den Werten anderer verwalteter Objekte inkonsistent ist.<br/> |



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
</dt> </dl>

 

