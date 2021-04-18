---
description: Die Tabelle "Aktions Text" enthält Text, der in einem Status Dialogfeld angezeigt und in das Protokoll geschrieben wird, um Aktionen auszuführen, deren Ausführung viel Zeit in Anspruch nimmt. Der angezeigte Text besteht aus der Aktions Beschreibung und optional formatierten Daten aus der Aktion.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabelle "aktiontext"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351640"
---
# <a name="actiontext-table"></a>Tabelle "aktiontext"

Die Tabelle "Aktions Text" enthält Text, der in einem Status Dialogfeld angezeigt und in das Protokoll geschrieben wird, um Aktionen auszuführen, deren Ausführung viel Zeit in Anspruch nimmt. Der angezeigte Text besteht aus der Aktions Beschreibung und optional formatierten Daten aus der Aktion.

Die Tabelle "aktiontext" enthält die folgenden Spalten.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Aktion      | [Bezeichner](identifier.md) | J   | N        |
| BESCHREIBUNG | [Text](text.md)             | N   | J        |
| Vorlage    | [Vorlage](template.md)     | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Name der Aktion.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Lokalisierte Beschreibung, die im Dialogfeld "Status" angezeigt wird oder in das Protokoll geschrieben wird, wenn die Aktion ausgeführt wird.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Fungiert
</dt> <dd>

Eine lokalisierte Formatvorlage, mit der Aktions Datensätze formatiert werden, die während der Ausführung der Aktion angezeigt werden. Wenn keine Vorlage bereitgestellt wird, werden die Aktions Daten nicht angezeigt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In der Regel beziehen sich die Einträge in der Tabelle "Aktions Text" auf Aktionen in Sequenz Tabellen. Der Installer führt andere Aktionen aus, die nicht in der Sequenz Tabelle aufgeführt sind, aber trotzdem in der Tabelle angegeben werden müssen. In der folgenden Tabelle sind die erforderlichen Tabelleneinträge aufgeführt, in denen der Aktionsname und die Vorlage genau wie gezeigt erstellt werden müssen, aber die Beschreibung kann angepasst werden.



| Aktion          | BESCHREIBUNG                             | Vorlage |
|-----------------|-----------------------------------------|----------|
| Rollback        | Macht Aktionen aus.                         | \[1\]    |
| Rollbackcleanup | Entfernt alte Dateien.                      | \[1\]    |
| Generatescript  | Generiert System Vorgänge für-Aktionen. | \[1\]    |



 

> [!Note]  
> Der Aktions Text wird nur für Aktionen angezeigt, die innerhalb des Installations Skripts ausgeführt werden. Daher wird der Aktions Text nur für Aktionen angezeigt, die zwischen den Aktionen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) sequenziert werden.

 

Sie können eine lokalisierte Aktions Text Tabelle mithilfe von Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)in die-Datenbank importieren. Das SDK enthält eine lokalisierte Aktions Text Tabelle für jede der Sprachen, die im Abschnitt [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) aufgeführt sind. Wenn die Aktions Text Tabelle nicht aufgefüllt ist, lädt das Installationsprogramm lokalisierte Zeichen folgen für die Sprache, die von der [**productlanguage**](productlanguage.md) -Eigenschaft angegeben wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



