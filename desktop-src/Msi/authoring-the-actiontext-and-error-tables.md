---
description: Die Beispielspezifikationen umfassen das Senden von ActionData-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und das Melden eines Fehlers, wenn ein Konto nicht erstellt werden kann.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Erstellen der ActionText- und Fehlertabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b89c8150e3767841fe914cf55fc7be8c92e8cecf8f54f8486993d955349be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045400"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Erstellen der ActionText- und Fehlertabellen

Die Beispielspezifikationen umfassen das Senden von ActionData-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und das Melden eines Fehlers, wenn ein Konto nicht erstellt werden kann.

Geben Sie die folgenden Einträge in die Tabelle ActionText ein, um informationen zu erhalten, die von ActionText-Meldungen verwendet werden.

[ActionText-Tabelle](actiontext-table.md)



| Aktion            | BESCHREIBUNG                                                       | Vorlage                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Generieren von Aktionen zum Erstellen von Benutzerkonten auf dem lokalen Computer. | Konto: \[ 1 \] , Attribute: \[ 2\] |
| CreateAccount     | Erstellen eines Benutzerkontos auf dem lokalen Computer.                      | Konto: \[ 1\]                    |
| RemoveAccount     | Entfernen des Benutzerkontos vom lokalen Computer.                    | Konto: \[ 1\]                    |
| RollbackAccount   | Roll back the creation of user accounts on the local computer. (Roll back the creation of user accounts on the local computer.) (Roll back the creation of user accounts on the local computer | Konto: \[ 1\]                    |
| UninstallAccounts | Generieren von Aktionen zum Entfernen von Benutzerkonten auf dem lokalen Computer. | Konto: \[ 1\]                    |



 

Geben Sie die folgenden Einträge in die Tabelle Fehler ein, um Informationen für die Fehlerberichterstattung zu erhalten.

[Fehlertabelle](error-table.md)



| Fehler | `Message`                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Das Benutzerkonto \[ "2" kann auf dem \] lokalen Computer nicht erstellt werden. Fehlercode: \[ 3 \] . |
| 25002 | Das Benutzerkonto \[ "2" \] ist bereits auf dem lokalen Computer vorhanden.                      |
| 25003 | Das Benutzerkonto \[ "2" kann auf dem \] lokalen Computer nicht entfernt werden. Fehlercode: \[ 3 \] . |
| 25004 | Das Benutzerkonto \[ "2" \] ist auf dem lokalen Computer nicht vorhanden.                      |



 

Fahren Sie [mit dem Erstellen der InstallExecuteSequence-Tabelle fort.](authoring-the-installexecutesequence-table.md)

 

 



