---
description: Die Kompatibilitätsinfrastruktur verwendet eine Datenbank, um Probleme mit der Anwendungskompatibilität und deren Lösungen zu identifizieren.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Anwendungskompatibilitätsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787e8dbc9aa07bc8d466dae766c3fed406692dbd32e128123c4b37d9a7a5618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956159"
---
# <a name="application-compatibility-database"></a>Anwendungskompatibilitätsdatenbank

Die Kompatibilitätsinfrastruktur verwendet eine Datenbank, um Probleme mit der Anwendungskompatibilität und deren Lösungen zu identifizieren. Diese Datenbank ist eine indizierte Binärdatei mit der Erweiterung .sdb. Die Kompatibilitätsinfrastruktur stellt eine Programmierschnittstelle für den Zugriff auf die Datenbank bereit.

Kompatibilitätsprobleme können zur Laufzeit anwendungsspezifische Behoben werden. Jede in der Datenbank angegebene Anwendung enthält mindestens eine Komponente, die eine Lösung benötigt. Komponenten sind ausführbare Dateien, die im Allgemeinen mit ihren Dateiattributen (z. B. Prüfsumme) beschrieben werden.

Der Prozess der Datenbanksuche und der Ermittlung der Lösungen für jede Anwendung wird als Abgleich *bezeichnet.* Die Dateiattribute und das Vorhandensein zugeordneter Dateien im Ordner oder Unterordner, der die .exe enthält, können verwendet werden, um eine eindeutige Übereinstimmung zu erstellen. Die zugeordneten Dateien werden als *übereinstimmende Dateien bezeichnet.*

Ein *TAG* ist ein eindeutiger Bezeichner für die Einträge und Attribute in der Datenbank. Der *TAG-Typ* gibt das Format der Daten an, die dem [**TAG zugeordnet sind.**](tag.md) Tagname ist **\_ beispielsweise** vom Typ **TAG TYPE \_ \_ STRINGREF.** Die Daten für **TAG \_ NAME** sind eine Namenszeichenfolge. Eine *TAGID* ist ein Zeiger auf einen Eintrag in einer bestimmten Datenbank. Ein *TAGREF-Element* ist ein Zeiger auf einen Eintrag, der datenbankübergreifend verwendet werden kann.

*Dateiattribute sind* Metadaten, die einer Datei auf dem Datenträger zugeordnet sind. Diese Attribute umfassen den Dateinamen, die Dateigröße, die Prüfsumme, die Version und das Datum. Diese Attribute werden verwendet, um zu bestimmen, ob eine vom System geladene Datei mit einem Datenbankeintrag entspricht. Daher werden diese Dateiattribute auch als *übereinstimmende Attribute bezeichnet.*

## <a name="solutions"></a>Lösungen

Die gängigsten Lösungen, die auf die Komponenten einer Anwendung angewendet werden, sind Apphelp und Appfix.

Mit Apphelp wird eine benutzerdefinierte lokalisierte Meldungsbenachrichtigung angezeigt, in der Regel, wenn die Anwendung installiert oder gestartet wird. Es enthält einen kurzen Text, der das Kompatibilitätsproblem erläutert und die Option zum Fortsetzen der Ausführung der Anwendung bietet. Einige Anwendungen werden jedoch erheblich ausfallen und dürfen ausgeführt werden. Apphelp gibt dem Benutzer nicht die Möglichkeit, diese Anwendungen weiter ausführen zu können.

Mit Appfix werden Hooks für APIs installiert, die von den Komponenten der Anwendung aufgerufen werden. Diese Hooks zeigen auf Stubfunktionen, die anstelle der Systemfunktionen aufgerufen werden können (auch als *Shimming bezeichnet).* Die Stubfunktionen führen Vorgänge aus, die erforderlich sind, damit die Anwendung auf der installierten Version von Windows. Jede Stubfunktion kann optional die Systemfunktion aufrufen, nachdem sie ihre Arbeit abgeschlossen hat. Eine *Kompatibilitätsebene* oder *ein Kompatibilitätsmodus* enthält einen oder mehrere Shims und Flags.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**\_APPHELP-DATEN**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**SUCHEN VON \_ INFORMATIONEN**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**PATH \_ TYPE**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNULLTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**Shim-Datenbanktypen**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**Etikett**](tag.md)
-   [**TAG-Typen**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



