---
description: Die SFPCatalog-Tabelle enthält die Kataloge, die von Windows Verwendet werden.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: SFPCatalog-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97498ff6437967a4a588be7b957aea130dad201699d55fad3abace6ff094b271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624891"
---
# <a name="sfpcatalog-table"></a>SFPCatalog-Tabelle

Die SFPCatalog-Tabelle enthält die Kataloge, die von Windows Verwendet werden.

Die Tabelle SFPCatalog enthält die folgenden Spalten.



| Spalte     | Typ                       | Key | Nullwerte zulässig |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Filename](filename.md)   | J   | N        |
| Katalog    | [Binär (Binary)](binary.md)       | N   | N        |
| Abhängigkeit | [Formatiert](formatted.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

Der kurze Dateiname für den Katalog. Da Kataloge keine Version haben, kann der in dieser Spalte angegebene Katalog einen Katalog überschreiben, der denselben Namen hat und bereits auf dem lokalen System installiert ist. Weitere Informationen finden Sie im Thema Zur Dateiversionsversionsierung [hat keine Datei eine Version.](neither-file-has-a-version.md)

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Katalog
</dt> <dd>

Binärdaten für den Katalog.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Abhängigkeit
</dt> <dd>

Der in diesem Feld angegebene Katalog ist das übergeordnete Element des abhängigen Katalogs, der im Feld SFPCatalog angegeben ist. Geben Sie den kurzen Dateinamen des übergeordneten Katalogs in das Feld Abhängigkeit ein. Dieses Feld ist ein Schlüssel zurück in die Spalte SFPCatalog. Bei der Abhängigkeits übereinstimmung wird die Kleinschreibung beachtet.

Wenn das Feld Abhängigkeit auf einen anderen Datensatz in dieser SFPCatalog-Tabelle verweist, wird der übergeordnete Katalog vor dem abhängigen Katalog installiert.

Wenn das Feld Abhängigkeit auf einen übergeordneten Katalog verweist, der nicht im Feld SFPCatalog dieser Tabelle vorhanden ist, und wenn der übergeordnete Katalog noch nicht installiert ist, schlägt die Installation fehl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [InstallSFPCatalogFile-Aktion](installsfpcatalogfile-action.md) fragt die [Component-Tabelle,](component-table.md)die [Dateitabelle,](file-table.md)die [FileSFPCatalog-Tabelle](filesfpcatalog-table.md) und die SFPCatalog-Tabelle ab.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



