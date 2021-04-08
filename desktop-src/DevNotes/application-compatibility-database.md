---
description: Die Kompatibilitäts Infrastruktur verwendet eine Datenbank, um Anwendungs Kompatibilitätsprobleme und ihre Lösungen zu identifizieren.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Anwendungs Kompatibilitätsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747968"
---
# <a name="application-compatibility-database"></a>Anwendungs Kompatibilitätsdatenbank

Die Kompatibilitäts Infrastruktur verwendet eine Datenbank, um Anwendungs Kompatibilitätsprobleme und ihre Lösungen zu identifizieren. Diese Datenbank ist eine indizierte Binärdatei mit der Erweiterung. SDB. Die Kompatibilitäts Infrastruktur stellt eine Programmierschnittstelle für den Zugriff auf die Datenbank bereit.

Kompatibilitätsprobleme können zur Laufzeit auf Anwendungs Basis behandelt werden. Jede in der Datenbank angegebene Anwendung enthält eine oder mehrere Komponenten, die eine Lösung benötigen. Komponenten sind ausführbare Dateien, die in der Regel mit ihren Dateiattributen (z. b. Checksum) beschrieben werden.

Der Prozess der Datenbanksuche und die Ermittlung der Lösungen für die einzelnen Anwendungen werden als *übereinstimmend* bezeichnet. Die Dateiattribute und das vorhanden sein von zugeordneten Dateien im Ordner oder Unterordner mit der exe-Datei können verwendet werden, um eine eindeutige Entsprechung zu erstellen. Die zugeordneten Dateien werden als *Übereinstimmende Dateien* bezeichnet.

Ein *Tag* ist ein eindeutiger Bezeichner für die Einträge und Attribute in der Datenbank. Der *Tagtyp* gibt das Format der Daten an, die dem [**Tag**](tag.md)zugeordnet sind. Der **\_ Tagname** ist z. b. vom Typ **\_ Tagtyp " \_ strauf**". die Daten für den **\_ Tagnamen** sind eine namens Zeichenfolge. Eine *TagID* ist ein Zeiger auf einen Eintrag in einer bestimmten Datenbank. Ein *tagref* ist ein Zeiger auf einen Eintrag, der über mehrere Datenbanken hinweg verwendet werden kann.

*Dateiattribute* sind Metadaten, die einer Datei auf dem Datenträger zugeordnet sind. Zu diesen Attributen gehören der Dateiname, die Dateigröße, die Prüfsumme, die Version und das Datum. Diese Attribute werden verwendet, um zu bestimmen, ob eine vom System geladene Datei mit einem Datenbankeintrag übereinstimmt. Daher werden diese Dateiattribute auch als *übereinstimmende Attribute* bezeichnet.

## <a name="solutions"></a>Lösungen

Die gängigsten Lösungen, die auf die Komponenten einer Anwendung angewendet werden, sind AppHelp und Appfix.

Mit AppHelp wird eine benutzerdefinierte lokalisierte Nachrichten Benachrichtigung angezeigt, in der Regel, wenn die Anwendung installiert oder gestartet wird. Es enthält kurzen Text, in dem das Kompatibilitätsproblem erläutert wird und die Option zum Fortsetzen der Ausführung der Anwendung bereit steht. Einige Anwendungen können jedoch nicht drastisch ausgeführt werden. AppHelp gibt dem Benutzer nicht die Möglichkeit, diese Anwendungen weiter zu ausführen.

Mit Appfix werden Hooks für APIs installiert, die von den Komponenten der Anwendung aufgerufen werden. Diese Hooks zeigen auf stubfunktionen, die anstelle der Systemfunktionen aufgerufen werden können (auch als *Shimmen* bezeichnet). Die Stub-Funktionen führen Vorgänge aus, die erforderlich sind, damit die Anwendung auf der installierten Version von Windows ausgeführt werden kann. Jede stubfunktion kann optional die Systemfunktion nach Abschluss ihrer Arbeit aufzurufen. Eine *Kompatibilitätsschicht* oder- *Modus* enthält ein oder mehrere Shims und Flags.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**AppHelp- \_ Daten**](apphelp-data.md)
-   [**Attrinfo**](attrinfo.md)
-   [**Baseflushappcompatcache**](baseflushappcompatcache.md)
-   [**\_Informationen suchen**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**\_Pfadtyp**](path-type.md)
-   [**Sdbbeginschreitelisttag**](sdbbeginwritelisttag.md)
-   [**Sdbclosedatabase**](sdbclosedatabase.md)
-   [**Sdbclosedatabasewrite**](sdbclosedatabasewrite.md)
-   [**Sdbcommitindexes**](sdbcommitindexes.md)
-   [**Sdbkreatedatabase**](sdbcreatedatabase.md)
-   [**Sdbdeclareingedex**](sdbdeclareindex.md)
-   [**Sdbendschreitelisttag**](sdbendwritelisttag.md)
-   [**Sdbfindfirstdwordindexedtag**](sdbfindfirstdwordindexedtag.md)
-   [**Sdbfindfirsttag**](sdbfindfirsttag.md)
-   [**Sdbfindnexttag**](sdbfindnexttag.md)
-   [**Sdbformatattribute**](sdbformatattribute.md)
-   [**Sdbfrefileattribute**](sdbfreefileattributes.md)
-   [**Sdbgetapppatchdir**](sdbgetapppatchdir.md)
-   [**Sdbgetbinarytagdata**](sdbgetbinarytagdata.md)
-   [**Sdbgetfileattribute**](sdbgetfileattributes.md)
-   [**Sdbgetfirstchild**](sdbgetfirstchild.md)
-   [**Sdbgetindex**](sdbgetindex.md)
-   [**Sdbgetmatchingexe**](sdbgetmatchingexe.md)
-   [**Sdbgetnextchild**](sdbgetnextchild.md)
-   [**Sdbgetstringtagptr**](sdbgetstringtagptr.md)
-   [**Sdbgettagfromtagid**](sdbgettagfromtagid.md)
-   [**Sdbinitdatabase**](sdbinitdatabase.md)
-   [**Sdbisstandarddatabase**](sdbisstandarddatabase.md)
-   [**Sdbmakeindexkeyfromstring**](sdbmakeindexkeyfromstring.md)
-   [**Sdbopenapphelpdetailsdatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**Sdbopenapphelpresourcefile**](sdbopenapphelpresourcefile.md)
-   [**Sdbopendatabase**](sdbopendatabase.md)
-   [**Sdbquerydataextagid**](sdbquerydataextagid.md)
-   [**Sdbqueryresult**](sdbqueryresult.md)
-   [**Sdbreadapphelpdetailsdata**](sdbreadapphelpdetailsdata.md)
-   [**Sdbreadbinarytag**](sdbreadbinarytag.md)
-   [**Sdbreaddwordtag**](sdbreaddwordtag.md)
-   [**Sdbreadqwordtag**](sdbreadqwordtag.md)
-   [**Sdbreadstringtag**](sdbreadstringtag.md)
-   [**Sdbregisterdatabaseex**](sdbregisterdatabaseex.md)
-   [**Sdbreleasedatabase**](sdbreleasedatabase.md)
-   [**Sdbreleasematchingexe**](sdbreleasematchingexe.md)
-   [**Sdbstartindizierung**](sdbstartindexing.md)
-   [**Sdbstopindizierung**](sdbstopindexing.md)
-   [**Sdbtagrebtotagid**](sdbtagreftotagid.md)
-   [**Sdbtagto String**](sdbtagtostring.md)
-   [**Sdbunregisterdatabase**](sdbunregisterdatabase.md)
-   [**Sdbschreitebinarytag**](sdbwritebinarytag.md)
-   [**Sdbschreitebinarytagfromfile**](sdbwritebinarytagfromfile.md)
-   [**Sdbschreitedwordtag**](sdbwritedwordtag.md)
-   [**Sdbschreitenulltag**](sdbwritenulltag.md)
-   [**Sdbschreiteqwordtag**](sdbwriteqwordtag.md)
-   [**Sdbschreitestringtag**](sdbwritestringtag.md)
-   [**Sdbschreitewordtag**](sdbwritewordtag.md)
-   [**Shim-Datenbanktypen**](shim-database-types.md)
-   [**Shimflushcache**](shimflushcache.md)
-   [**Tag**](tag.md)
-   [**Tagtypen**](tag-types.md)
-   [**TagID**](tagid.md)
-   [**Tagref**](tagref.md)

 

 



