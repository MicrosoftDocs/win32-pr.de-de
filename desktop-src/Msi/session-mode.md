---
description: Dies ist die Mode-Eigenschaft des Session-Objekts. Diese Eigenschaft ist ein Wert, der das Flag für den vorgesehenen Modus für die aktuelle Installationssitzung darstellt. Die meisten modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session. Mode (Eigenschaft)
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
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364530"
---
# <a name="sessionmode-property"></a>Session. Mode (Eigenschaft)

Dies ist die **Mode** -Eigenschaft des [**Session**](session-object.md) -Objekts. Diese Eigenschaft ist ein Wert, der das Flag für den vorgesehenen Modus für die aktuelle Installationssitzung darstellt. Die meisten modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.

Die [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) -Funktion gibt einen booleschen Wert "true" oder "false" zurück, der angibt, ob die angegebene Eigenschaft, die an die Funktion übertragen wird, aktuell festgelegt ist (true) oder nicht festgelegt

Beachten Sie, dass nicht alle runmoduswerte des *Flags* verfügbar sind, wenn die **Mode** -Eigenschaft aus einer verzögerten benutzerdefinierten Aktion aufgerufen wird. Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>Eigenschaftswert

Der erforderliche ganzzahlige Wert für das Flag. Dies muss eine der folgenden Ressourcen sein:



| Flagname                                                                                                                                                                                                                                                                                                | Bedeutung                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**msirun0deadmin**</dt> <dt>0</dt> </dl>                                              | Installation im administrativen Modus, sonst Produktinstallation.<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msirunmodeankündigungs**</dt> <dt>1</dt> </dl>                              | Ankündigungs Modus für die Installation.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msirunmodemaintenance**</dt> <dt>2</dt> </dl>                      | Wartungsmodus-Datenbank geladen.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msirunmoderollbackaktivierte**</dt> <dt>3</dt> </dl>      | Das Rollback ist aktiviert.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msirunmodelogenabled**</dt> <dt>4</dt> </dl>                          | Die Protokolldatei ist aktiv.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msirunmodeoperations**</dt> <dt>5</dt> </dl>                          | Ausführen oder spoolingvorgänge.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msirunmoderebootatend**</dt> <dt>6</dt> </dl>                      | Ein Neustart ist erforderlich (feststellbar).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msirunmoderebootnow**</dt> <dt>7</dt> </dl>                              | Zum Fortsetzen der Installation (feststellbar) ist ein Neustart erforderlich.<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msirunmadecabinet**</dt> <dt>8</dt> </dl>                                      | Installieren von Dateien aus kabinatendateien und Dateien mithilfe der Medien Tabelle.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msirunmodesourceshortnames**</dt> <dt>9</dt> </dl>  | Für Quelldateien werden nur kurze Dateinamen verwendet.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msirunmodetargetshortnames**</dt> <dt>10</dt> </dl> | Zieldateien sind nur kurze Dateinamen.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | Das Betriebssystem ist Windows 98/95.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msirunmodezawenabled**</dt> <dt>13</dt> </dl>                         | Das Betriebssystem unterstützt die Werbung von Produkten.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msirunmodescheduled**</dt> <dt>16</dt> </dl>                             | Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die von der Installationsskript Ausführung aufgerufen wurde.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msirunmoderollback**</dt> <dt>17</dt> </dl>                                 | Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die vom Rollback-Ausführungs Skript aufgerufen wurde.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msirunmodecommit**</dt> <dt>18</dt> </dl>                                         | Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die vom Commit-Ausführungs Skript aufgerufen wurde.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



 

 




