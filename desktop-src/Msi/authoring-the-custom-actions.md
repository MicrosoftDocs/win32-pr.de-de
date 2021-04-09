---
description: 'In der folgenden Tabelle sind die fünf benutzerdefinierten Aktionen aufgeführt, die zum erfüllen der Beispiel Spezifikationen verwendet werden: processaccounts, uninstallaccounts, kreateaccounts, removeaccounts und rollbackaccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Erstellen der benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09525490304762b98635bcbbe6c238ce3fe413f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959510"
---
# <a name="authoring-the-custom-actions"></a>Erstellen der benutzerdefinierten Aktionen

In der folgenden Tabelle sind die fünf benutzerdefinierten Aktionen aufgeführt, die zum erfüllen der Beispiel Spezifikationen verwendet werden: processaccounts, uninstallaccounts, kreateaccounts, removeaccounts und rollbackaccounts. Alle diese benutzerdefinierten Aktionen befinden sich in den in der [binären Tabelle](binary-table.md)gespeicherten [Dynamic-Link-Bibliotheken](dynamic-link-libraries.md) . Der C++-Quellcode für die Dynamic-Link-Bibliotheken, die die benutzerdefinierten Beispiel Aktionen enthalten, wird im Windows Installer SDK bereitgestellt. Processaccounts und uninstallaccounts befinden sich in der Datei Process. cpp. "Kreateaccount" befindet sich in der Datei "Create. cpp". Removeaccount und rollbackaccount befinden sich in der Datei Remove. cpp. Diese Quelldateien können zum Erstellen der Dateien Process.dll, Create.dll und Remove.dll verwendet werden.

Da das Erstellen oder Entfernen eines Benutzerkontos erhöhte Rechte erfordert, müssen Benutzer [definierte Aktionen mit verzögerter Ausführung](deferred-execution-custom-actions.md) , die im Kontext des Systems ausgeführt werden, zum Erstellen, entfernen oder Zurücksetzen von Benutzerkonten verwendet werden. Die benutzerdefinierten Aktionen direkt ausführen, processaccounts und uninstallaccounts generieren die verzögerten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder zurücksetzen: "kreateaccount", "removeaccount" und "rollbackaccount".

Da verzögerte benutzerdefinierte Aktionen keine Informationen in Datenbanktabellen lesen können, müssen processaccounts und uninstalluseraccouts eine customaktiondata-Eigenschaft festlegen, um die Informationen in der UserAccounts-Tabelle an die verzögerten benutzerdefinierten Aktionen zu übergeben, wie unter Abrufen [von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)beschrieben. Wenn das Installationsprogramm das Ausführungs Skript ausführt, behandeln die verzögerten benutzerdefinierten Aktionen Benutzerkonten entsprechend den Informationen in der customaktiondata-Eigenschaft.

Da alle benutzerdefinierten Aktionen in den in der binären Tabelle gespeicherten Dynamic-Link-Bibliotheken enthalten sind, enthalten Sie alle die Konstanten "msidbcustomaction typedll" und "msidbcustomaction typebinarydata" in ihren grundlegenden numerischen Typ. Processaccounts und uninstallaccounts sind Beispiele für den reinen [benutzerdefinierten Aktionstyp 1](custom-action-type-1.md). Informationen zu anderen benutzerdefinierten Aktions Typen finden Sie in der [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md).

Bei "kreateaccount" und "removeaccount" handelt es sich um [benutzerdefinierte Aktionen](deferred-execution-custom-actions.md) , mit denen die Identität bestimmter Benutzer nicht angenommen werden kann. Diese benutzerdefinierten Aktionen umfassen die Konstanten msidbcustomaction typeinscript und msidbcustomaction typoidentitäts ATE, um diese [benutzerdefinierte Aktion in-Script-Ausführungs Optionen](custom-action-in-script-execution-options.md)anzugeben.

Rollbackaccount ist eine [benutzerdefinierte Rollback-Aktion](rollback-custom-actions.md) , die Benutzerkonten nur während einer [Rollback-Installation](rollback-installation.md)entfernt. Rollbackaccount schließt die Konstanten msidbcustomaction typeinscript und msidbcustomaction typerollback ein, um diese [benutzerdefinierte Aktion in-Script-Ausführungs Optionen](custom-action-in-script-execution-options.md)anzugeben.

Diese benutzerdefinierten Aktionen verarbeiten möglicherweise sensible Daten, z. b. Benutzer Kennwörter, die nicht in die Protokolldatei geschrieben werden sollten. Die verzögerten benutzerdefinierten Aktionen sollten daher "msidbcustomaction typehidetarget" in den Typ "benutzerdefinierte Aktion" einschließen. Aufgrund der Art und Weise, wie unmittelbare benutzerdefinierte Aktionen mithilfe der customaktiondata-Eigenschaft Daten an verzögerte benutzerdefinierte Aktionen übergeben, müssen die Namen der verzögerten benutzerdefinierten Aktionen auch der Eigenschaften Liste " [**msihiddenproperties**](msihiddenproperties.md) " in der Eigenschaften [Tabelle](property-table.md) hinzugefügt werden.



| Benutzerdefinierte Aktion     | DLL-Einstiegspunkt                       | Benutzerdefinierter Aktionstyp                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Processaccounts   | Processuseraccounts in Process.dll.   | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata = 1                                                                                                             |
| Nicht installaccounts | Uninstalluseraccounts in Process.dll. | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata = 1                                                                                                             |
| CreateAccount     | "Kreateuseraccount" in "Create.dll".      | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypeingescript + msidbcustomaktiontypoidentitäts Ate + msidbcustomaktiontypehidetarget = 11265. |
| RemoveAccount     | Removeuseraccount in Remove.dll.      | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypeingescript + msidbcustomaktiontypoidentitäts Ate + msidbcustomaktiontypehidetarget = 11265. |
| Rollbackaccount   | Removeuseraccount in Remove.dll.      | msidbcustomaktiontypedll + msidbcustomaktiontypebinarydata + msidbcustomaktiontypeingescript + msidbcustomaktiontyperollback + msidbcustomaktiontypehidetarget = 9473.       |



 

Fahren Sie mit [dem Erstellen der Tabelle CustomAction](authoring-the-customaction-table.md)fort.

 

 



