---
description: Dies ist die Mode-Eigenschaft des Session-Objekts. Diese Eigenschaft ist ein Wert, der das Flag für den festgelegten Modus für die aktuelle Installationssitzung darstellt. Die meisten Modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session.Mode(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed0c24280307cf368239ab88b5357924a3ee40d5a62444838e155aca2c0642f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629120"
---
# <a name="sessionmode-property"></a>Session.Mode(Eigenschaft)

Dies ist **die Mode-Eigenschaft** des [**Session-Objekts.**](session-object.md) Diese Eigenschaft ist ein Wert, der das Flag für den festgelegten Modus für die aktuelle Installationssitzung darstellt. Die meisten Modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.

Die [**MsiGetMode-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) gibt einen booleschen TRUE- oder FALSE-Wert zurück, der angibt, ob die an die Funktion übergebene spezifische Eigenschaft derzeit festgelegt (TRUE) oder nicht festgelegt ist (FALSE).

Beachten Sie, dass nicht alle Ausführungsmoduswerte des Flags verfügbar *sind,* wenn die **Mode-Eigenschaft** aus einer verzögerten benutzerdefinierten Aktion aufruft. Weitere Informationen finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher ganzzahliger Wert für das Flag. Dies muss eine der folgenden Ressourcen sein:



| Flagname                                                                                                                                                                                                                                                                                                | Bedeutung                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**msiRunModeAdmin**</dt> <dt>0</dt> </dl>                                              | Installation im Verwaltungsmodus, sonst Produkt installieren.<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msiRunModeAdvertise**</dt> <dt>1</dt> </dl>                              | Ankündigungsmodus der Installation.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msiRunModeMaintenance**</dt> <dt>2</dt> </dl>                      | Geladene Datenbank im Wartungsmodus.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt> </dl>      | Rollback ist aktiviert.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msiRunModeLogEnabled**</dt> <dt>4</dt> </dl>                          | Die Protokolldatei ist aktiv.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msiRunModeOperations**</dt> <dt>5</dt> </dl>                          | Ausführen oder Spoolen von Vorgängen.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt> </dl>                      | Ein Neustart ist erforderlich (festlegbar).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msiRunModeRebootNow**</dt> <dt>7</dt> </dl>                              | Ein Neustart ist erforderlich, um die Installation (festlegbar) fortsetzen zu können.<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msiRunModeCabinet**</dt> <dt>8</dt> </dl>                                      | Installieren von Dateien aus Schränken und Dateien mithilfe der Medientabelle.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt> </dl>  | Quelldateien verwenden nur kurze Dateinamen.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt> </dl> | Zieldateien sollen nur kurze Dateinamen verwenden.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | Das Betriebssystem ist Windows 98/95 installiert.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msiRunModeZawEnabled**</dt> <dt>13</dt> </dl>                         | Das Betriebssystem unterstützt die Werbung für Produkte.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msiRunModeScheduled**</dt> <dt>16</dt> </dl>                             | Verzögerte [benutzerdefinierte Aktion,](custom-actions.md) die von der Ausführung des Installationsskripts aufgerufen wird.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msiRunModeRollback**</dt> <dt>17</dt> </dl>                                 | Verzögerte [benutzerdefinierte Aktion,](custom-actions.md) die vom Rollbackausführungsskript aufgerufen wird.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msiRunModeCommit**</dt> <dt>18</dt> </dl>                                         | Verzögerte [benutzerdefinierte Aktion, die](custom-actions.md) vom Commitausführungsskript aufgerufen wird.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



 

 




