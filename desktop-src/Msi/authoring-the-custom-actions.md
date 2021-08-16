---
description: 'In der folgenden Tabelle sind die fünf benutzerdefinierten Aktionen aufgeführt, die verwendet werden, um die Beispielspezifikationen zu erfüllen: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts und RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Erstellen der benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6880f95b0468a495653057a9a5802af671c55b18b025c38a3191a4792e7558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381175"
---
# <a name="authoring-the-custom-actions"></a>Erstellen der benutzerdefinierten Aktionen

In der folgenden Tabelle sind die fünf benutzerdefinierten Aktionen aufgeführt, die verwendet werden, um die Beispielspezifikationen zu erfüllen: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts und RollbackAccounts. Alle diese benutzerdefinierten Aktionen befinden sich in Dynamic [Link-Bibliotheken, die](dynamic-link-libraries.md) in der [Binärtabelle gespeichert sind.](binary-table.md) Der C++-Quellcode für die Dynamic Link-Bibliotheken, die die benutzerdefinierten Beispielaktionen enthalten, finden Sie im Windows Installer SDK. ProcessAccounts und UninstallAccounts befinden sich in der Datei Process.cpp. CreateAccount befindet sich in der Datei Create.cpp. RemoveAccount und RollbackAccount befinden sich in der Datei Remove.cpp. Diese Quelldateien können verwendet werden, um die Dateien Process.dll, Create.dll und Remove.dll.

Da das Erstellen oder Entfernen eines Benutzerkontos erhöhte Rechte [erfordert,](deferred-execution-custom-actions.md) müssen benutzerdefinierte Aktionen zur verzögerten Ausführung, die im Kontext des Systems ausgeführt werden, zum Erstellen, Entfernen oder Rollback von Benutzerkonten verwendet werden. Die benutzerdefinierten Sofortausführungsaktionen ProcessAccounts und UninstallAccounts generieren die zurückgestellten benutzerdefinierten Aktionen zum Erstellen, Entfernen oder Rollback von Benutzerkonten: CreateAccount, RemoveAccount und RollbackAccount.

Da verzögerte benutzerdefinierte Aktionen keine Informationen in Datenbanktabellen lesen können, müssen ProcessAccounts und UninstallUserAccouts eine CustomActionData-Eigenschaft festlegen, um die Informationen in der Tabelle UserAccounts an die zurückgestellten benutzerdefinierten Aktionen zu übergeben, wie unter [Abrufen](obtaining-context-information-for-deferred-execution-custom-actions.md)von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung beschrieben. Wenn das Installationsprogramm das Ausführungsskript ausgeführt, verarbeiten die verzögerten benutzerdefinierten Aktionen Benutzerkonten gemäß den Informationen in der CustomActionData-Eigenschaft.

Da sich alle benutzerdefinierten Aktionen in Dynamic Link-Bibliotheken befinden, die in der Binary-Tabelle gespeichert sind, enthalten sie alle die Konstanten msidbCustomActionTypeDll und msidbCustomActionTypeBinaryData in ihrem numerischen Basistyp. ProcessAccounts und UninstallAccounts sind Beispiele für rein [benutzerdefinierten Aktionstyp 1.](custom-action-type-1.md) Informationen zu anderen benutzerdefinierten Aktionstypen finden Sie in der [Zusammenfassungsliste aller benutzerdefinierten Aktionstypen.](summary-list-of-all-custom-action-types.md)

CreateAccount und RemoveAccount sind benutzerdefinierte Aktionen mit verzögerter [Ausführung,](deferred-execution-custom-actions.md) die es Diensten nicht ermöglichen, die Identität bestimmter Benutzer zu imitieren. Zu diesen benutzerdefinierten Aktionen gehören die Konstanten msidbCustomActionTypeInScript und msidbCustomActionTypeNoImpersonate, um diese benutzerdefinierten [Aktionsausführungsoptionen im Skript anzugeben.](custom-action-in-script-execution-options.md)

RollbackAccount ist eine [benutzerdefinierte Rollbackaktion,](rollback-custom-actions.md) die Benutzerkonten nur während einer [Rollbackinstallation entfernt.](rollback-installation.md) RollbackAccount enthält die Konstanten msidbCustomActionTypeInScript und msidbCustomActionTypeRollback, um diese benutzerdefinierten [Aktionsausführungsoptionen im Skript anzugeben.](custom-action-in-script-execution-options.md)

Diese benutzerdefinierten Aktionen können vertrauliche Daten verarbeiten, z. B. Benutzerkennwörter, die nicht in die Protokolldatei geschrieben werden sollten. Die zurückgestellten benutzerdefinierten Aktionen sollten daher msidbCustomActionTypeHideTarget im benutzerdefinierten Aktionstyp enthalten. Die Namen der zurückgestellten benutzerdefinierten Aktionen müssen auch der [**Eigenschaftenliste MsiHiddenProperties**](msihiddenproperties.md) in der [Property](property-table.md) -Tabelle hinzugefügt werden, da sofortige benutzerdefinierte Aktionen Daten mithilfe der CustomActionData-Eigenschaft an zurückgestellte benutzerdefinierte Aktionen übergeben.



| Benutzerdefinierte Aktion     | DLL-Einstiegspunkt                       | Benutzerdefinierter Aktionstyp                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts in Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts in Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount in Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Fahren Sie mit [dem Erstellen der CustomAction-Tabelle fort.](authoring-the-customaction-table.md)

 

 



