---
title: SNMP-Fehler Codes (SNMP. h)
description: Microsoft implementiert die folgenden SNMP-Fehlercodes, die in der SNMPv2C-Spezifikation definiert sind.
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
ms.openlocfilehash: 17c1ec7a25490737dd31b2962c09d2e0f36c72d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040210"
---
# <a name="snmp-error-codes"></a>SNMP-Fehler Codes

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Microsoft implementiert die folgenden SNMP-Fehlercodes, die in der SNMPv2C-Spezifikation definiert sind.



| Konstante/Wert                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ ErrorStatus \_ noError**</dt> <dt>0</dt> </dl>                                      | Der Agent meldet, dass während der Übertragung keine Fehler aufgetreten sind.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ ErrorStatus \_**</dt> -Wert <dt>1</dt> </dl>                                         | Der Agent konnte die Ergebnisse des angeforderten SNMP-Vorgangs nicht in einer einzelnen SNMP-Nachricht platzieren.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ ErrorStatus \_ nosuchname**</dt> <dt>2</dt> </dl>                             | Der angeforderte SNMP-Vorgang hat eine unbekannte Variable identifiziert.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ ErrorStatus \_ badvalue**</dt> <dt>3</dt> </dl>                                   | Der angeforderte SNMP-Vorgang hat versucht, eine Variable zu ändern, hat jedoch entweder einen Syntax-oder einen Wert Fehler angegeben.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ ErrorStatus \_**</dt> schreibgeschützt <dt>4</dt> </dl>                                   | Der angeforderte SNMP-Vorgang hat versucht, eine Variable zu ändern, die gemäß dem communityprofil der Variablen nicht geändert werden konnte.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ ErrorStatus \_ generr**</dt> <dt>5</dt> </dl>                                         | Bei dem angeforderten SNMP-Vorgang ist ein anderer Fehler als einer der hier aufgeführten Fehler aufgetreten.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ ErrorStatus \_ NoAccess**</dt> <dt>6</dt> </dl>                                   | Auf die angegebene SNMP-Variable kann nicht zugegriffen werden.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ ErrorStatus- \_ Fehlertyp**</dt> <dt>7</dt> </dl>                                | Der Wert gibt einen Typ an, der nicht mit dem für die Variable erforderlichen Typ konsistent ist.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ ErrorStatus- \_ fehlerhafte Fehler**</dt> Meldung <dt>8</dt> </dl>                          | Der Wert gibt eine Länge an, die nicht mit der für die Variable erforderlichen Länge konsistent ist.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ ErrorStatus- \_ Fehlercode**</dt> <dt>9</dt> </dl>                    | Der-Wert enthält eine ASN. 1-Codierung (Abstract Syntax Notation One), die nicht mit dem ASN. 1-Tag des Felds konsistent ist.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ ErrorStatus \_**</dt> -Fehlerwert <dt>10</dt> </dl>                            | Der Wert kann der Variablen nicht zugewiesen werden.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ ErrorStatus- \_ nocreation**</dt> <dt>11</dt> </dl>                            | Die Variable ist nicht vorhanden, und Sie kann vom Agent nicht erstellt werden.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ ErrorStatus \_ inkonsistentvalue**</dt> <dt>12</dt> </dl>       | Der Wert ist nicht mit den Werten anderer verwalteter Objekte konsistent.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ ErrorStatus \_ resourcenicht verfügbar**</dt> <dt>13</dt> </dl> | Das Zuweisen des Werts zur Variablen erfordert die Zuweisung von Ressourcen, die zurzeit nicht verfügbar sind.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ ErrorStatus \_ commitfailed**</dt> <dt>14</dt> </dl>                      | Es sind keine Validierungs Fehler aufgetreten, aber es wurden keine Variablen aktualisiert.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ ErrorStatus \_ undofailed**</dt> <dt>15</dt> </dl>                            | Es sind keine Validierungs Fehler aufgetreten. Einige Variablen wurden aktualisiert, weil die Zuweisung nicht rückgängig gemacht werden konnte.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ ErrorStatus- \_ authorizationerror**</dt> <dt>16</dt> </dl>    | Ein Autorisierungs Fehler ist aufgetreten.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ ErrorStatus \_ notschreibtabelle**</dt> <dt>17</dt> </dl>                         | Die Variable ist vorhanden, der Agent kann Sie jedoch nicht ändern.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ ErrorStatus \_ inkonsistentname**</dt> <dt>18</dt> </dl>          | Die Variable ist nicht vorhanden. der Agent kann ihn nicht erstellen, da die benannte Objektinstanz nicht mit den Werten anderer verwalteter Objekte konsistent ist.<br/> |



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
</dt> </dl>

 

