---
description: Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts generieren die verzögerten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder zurücksetzen.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Erstellen der InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358852"
---
# <a name="authoring-the-installexecutesequence-table"></a>Erstellen der InstallExecuteSequence-Tabelle

Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts generieren die verzögerten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder zurücksetzen. Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts müssen in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) eingegeben werden, die ausgeführt werden soll. Fügen Sie die folgenden Einträge der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)hinzu. Da diese benutzerdefinierten Aktionen Teil der Skript Generierung sein müssen, müssen beide benutzerdefinierten Aktionen nach der [InstallInitialize-Aktion](installinitialize-action.md)sequenziert werden.

Die Bedingung für processaccounts stellt Folgendes sicher: Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).

-   Processaccounts wird nur ausgeführt, wenn die Komponente Testaccount lokal auf dem Computer installiert wird.
-   Das Komponenten Test Konto ist zurzeit nicht installiert oder wird zum Ausführen von der Quelle installiert.

Die Bedingung für uninstallaccount stellt Folgendes sicher:

-   Uninstallaccounts werden nur ausgeführt, wenn die Komponente Testaccount lokal auf dem Computer installiert ist.
-   Das Komponenten Test Konto wird entfernt oder zum Ausführen von der Quelle installiert.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion            | Bedingung                                                           | Sequenz |
|-------------------|---------------------------------------------------------------------|----------|
| Processaccounts   | VersionNT und (? Testaccount = 2 oder? Testaccount = 4) und $TestAccount = 3 | 1550     |
| Nicht installaccounts | VersionNT und? Testaccount = 3 und ($TestAccount = 4 oder $TestAccount = 2) | 1560     |



 

Erstellen Sie [die Benutzeroberfläche für die Kenn Wort Eingabe](authoring-the-user-interface-for-password-input.md)weiter.

 

 



