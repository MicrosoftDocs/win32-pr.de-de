---
description: Die sfpcatalog-Tabelle enthält die von Windows Me verwendeten Kataloge.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Sfpcatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214858"
---
# <a name="sfpcatalog-table"></a>Sfpcatalog-Tabelle

Die sfpcatalog-Tabelle enthält die von Windows Me verwendeten Kataloge.

Die sfpcatalog-Tabelle weist die folgenden Spalten auf.



| Spalte     | Typ                       | Schlüssel | Nullwerte zulässig |
|------------|----------------------------|-----|----------|
| Sfpcatalog | [Filename](filename.md)   | J   | N        |
| Katalog    | [Binär (Binary)](binary.md)       | N   | N        |
| Abhängigkeit | [Großformatige](formatted.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>Sfpcatalog
</dt> <dd>

Der kurze Dateiname für den Katalog. Da Kataloge keine Version aufweisen, kann der in dieser Spalte angegebene Katalog einen Katalog überschreiben, der denselben Namen hat und bereits auf dem lokalen System installiert ist. Weitere Informationen finden Sie [im Thema zur Datei Versions](neither-file-has-a-version.md)Verwaltung.

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren
</dt> <dd>

Binärdaten für den Katalog.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Gkeit
</dt> <dd>

Der in diesem Feld angegebene Katalog ist das übergeordnete Element des abhängigen Katalogs, der im Feld sfpcatalog angegeben ist. Geben Sie den kurzen Dateinamen des übergeordneten Katalogs in das Abhängigkeits Feld ein. Dieses Feld ist ein Schlüssel zurück in die sfpcatalog-Spalte. Bei der Abhängigkeit wird die Groß-/Kleinschreibung beachtet.

Wenn das Abhängigkeits Feld auf einen anderen Datensatz in dieser sfpcatalog-Tabelle verweist, wird der übergeordnete Katalog vor dem abhängigen Katalog installiert.

Wenn das Abhängigkeits Feld auf einen übergeordneten Katalog verweist, der im Feld sfpcatalog der Tabelle nicht vorhanden ist, und wenn der übergeordnete Katalog nicht bereits installiert ist, tritt bei der Installation ein Fehler auf.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der [Aktion installsfpcatalogfile](installsfpcatalogfile-action.md) werden die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die [filesfpcatalog-Tabelle](filesfpcatalog-table.md) und die sfpcatalog-Tabelle abgefragt.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



