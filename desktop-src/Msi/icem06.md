---
description: ICEM06 prüft auf ungültige direkte Verweise auf Features durch das Modul.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865763"
---
# <a name="icem06"></a>ICEM06

ICEM06 prüft auf ungültige direkte Verweise auf Features durch das Modul.

Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb

## <a name="result"></a>Ergebnis

ICEM06 gibt einen Fehler aus, wenn die Modul Datenbank direkte Verweise auf eine Funktion enthält. Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden.

## <a name="example"></a>Beispiel

ICEM06 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung          | Ziel                                 |
|-------------------|----------------------------------------|
| Shortcut1. *Guid1* | cmd.exe                                |
| Shortcut2. *Guid1* | \[MyProp\]                             |
| Shortcut3. *Guid1* | {00000000-0000-0000-0000-000000000000} |



 

[Klassen Tabelle](class-table.md) (partiell)



| CLSID   | Kontext       | Komponente\_ | Funktion\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | Myfeature                              |



 

ICEM06 meldet den ersten Fehler, da der erste Datensatz in der Verknüpfungs Tabelle über einen Eintrag im Zielfeld verfügt, der keine Eigenschaft oder NULL-GUID ist. Ein Modul kann nicht direkt auf eine Funktion verweisen. Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden. Um diesen Fehler zu beheben, müssen Verweise auf eine Funktion durch eine NULL-GUID ersetzt werden.

ICEM06 meldet den zweiten Fehler, da der zweite Datensatz in der Klassen Tabelle über einen Eintrag im Funktionsfeld verfügt, der keine NULL-GUID ist. Ein Modul kann nicht direkt auf eine Funktion verweisen. Funktions Informationen müssen vom Benutzer des Moduls bereitgestellt werden. Um diesen Fehler zu beheben, müssen Verweise auf eine Funktion durch eine NULL-GUID ersetzt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



