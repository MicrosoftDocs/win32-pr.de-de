---
description: Die benutzerdefinierten Aktionen ProcessAccounts und UninstallAccounts generieren die zurückgestellten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder rollbacken.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Erstellen der InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ff6b8a551b141b5fc3f4d15318f2a6d98ff834cd33a572d542563adf55447b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639171"
---
# <a name="authoring-the-installexecutesequence-table"></a>Erstellen der InstallExecuteSequence-Tabelle

Die benutzerdefinierten Aktionen ProcessAccounts und UninstallAccounts generieren die zurückgestellten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder rollbacken. Die benutzerdefinierten Aktionen ProcessAccounts und UninstallAccounts müssen in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) eingegeben werden, um ausgeführt werden zu können. Fügen Sie der [Tabelle InstallExecuteSequence die folgenden Einträge hinzu.](installexecutesequence-table.md) Da diese benutzerdefinierten Aktionen Teil der Skriptgenerierung sein müssen, müssen beide benutzerdefinierten Aktionen nach der [InstallInitialize-Aktion sequenziert werden.](installinitialize-action.md)

Die Bedingung für ProcessAccounts stellt Folgendes sicher. Weitere Informationen finden [Sie unter Syntax für bedingte Anweisungen.](conditional-statement-syntax.md)

-   ProcessAccounts wird nur ausgeführt, wenn die Komponente TestAccount lokal auf dem Computer installiert wird.
-   Das Komponententestkonto ist derzeit nicht installiert oder für die Ausführung über die Quelle installiert.

Die Bedingung für UninstallAccount stellt Folgendes sicher:

-   UninstallAccounts wird nur ausgeführt, wenn die Komponente TestAccount lokal auf dem Computer installiert ist.
-   Das Komponententestkonto wird entfernt oder installiert, um aus der Quelle ausgeführt zu werden.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion            | Bedingung                                                           | Sequenz |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT AND (? TestAccount=2 OR ? TestAccount=4) AND $TestAccount=3 | 1550     |
| UninstallAccounts | VersionNT UND ? TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2) | 1560     |



 

Fahren Sie mit [Erstellen der Benutzeroberfläche für die Kennworteingabe fort.](authoring-the-user-interface-for-password-input.md)

 

 



