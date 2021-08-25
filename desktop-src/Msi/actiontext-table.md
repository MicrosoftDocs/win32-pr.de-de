---
description: Die ActionText-Tabelle enthält Text, der in einem Statusdialogfeld angezeigt und in das Protokoll für Aktionen geschrieben wird, die lange dauern. Der angezeigte Text besteht aus der Aktionsbeschreibung und optional formatierten Daten aus der Aktion.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: ActionText-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21923588676db4ad38482768a493428ce76caf32b32334e429fbe41335c2bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927260"
---
# <a name="actiontext-table"></a>ActionText-Tabelle

Die ActionText-Tabelle enthält Text, der in einem Statusdialogfeld angezeigt und in das Protokoll für Aktionen geschrieben wird, die lange dauern. Der angezeigte Text besteht aus der Aktionsbeschreibung und optional formatierten Daten aus der Aktion.

Die ActionText-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Aktion      | [Identifier](identifier.md) | J   | N        |
| BESCHREIBUNG | [Text](text.md)             | N   | J        |
| Vorlage    | [Vorlage](template.md)     | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Name der Aktion.

Primärer Tabellenschlüssel.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Lokalisierte Beschreibung, die im Statusdialogfeld angezeigt oder beim Ausführen der Aktion in das Protokoll geschrieben wird.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Vorlage
</dt> <dd>

Eine lokalisierte Formatvorlage, die zum Formatieren von Aktionsdatensätzen verwendet wird, die während der Aktionsausführung angezeigt werden. Wenn keine Vorlage bereitgestellt wird, werden die Aktionsdaten nicht angezeigt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In der Regel verweisen die Einträge in der ActionText-Tabelle auf Aktionen in Sequenztabellen. Es gibt andere Aktionen, die das Installationsprogramm ausführt, die nicht in der Sequenztabelle aufgeführt sind, aber dennoch in der Tabelle angegeben werden müssen. In der folgenden Tabelle sind die erforderlichen Tabelleneinträge aufgeführt, bei denen der Aktionsname und die Vorlage genau wie gezeigt erstellt werden müssen, aber die Beschreibung angepasst werden kann.



| Aktion          | BESCHREIBUNG                             | Vorlage |
|-----------------|-----------------------------------------|----------|
| Rollback        | Rückgängig machen von Aktionen.                         | \[1\]    |
| RollbackCleanup | Entfernt alte Dateien.                      | \[1\]    |
| GenerateScript  | Generiert Systemvorgänge für Aktionen. | \[1\]    |



 

> [!Note]  
> Aktionstext wird nur für Aktionen angezeigt, die innerhalb des Installationsskripts ausgeführt werden. Aus diesem Grund wird Aktionstext nur für Aktionen angezeigt, die zwischen den [Aktionen InstallInitialize](installinitialize-action.md) und [InstallFinalize sequenziert](installfinalize-action.md) werden.

 

Sie können eine lokalisierte ActionText-Tabelle in Ihre Datenbank importieren, indem Sie Msidb.exe [**oder MsiDatabaseImport verwenden.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) Das SDK enthält eine lokalisierte ActionText-Tabelle für jede der Sprachen, die im Abschnitt [Lokalisieren der Fehler- und Aktionstexttabellen aufgeführt](localizing-the-error-and-actiontext-tables.md) sind. Wenn die ActionText-Tabelle nicht aufgefüllt wird, lädt das Installationsprogramm lokalisierte Zeichenfolgen für die Sprache, die von der [**ProductLanguage-Eigenschaft angegeben**](productlanguage.md) wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



