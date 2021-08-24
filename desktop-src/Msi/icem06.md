---
description: ICEM06 überprüft vom Modul auf ungültige direkte Verweise auf Features.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5150e511e6f8018e51ab537b52ccc6c32645d09c80110129f040d6a329335ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828880"
---
# <a name="icem06"></a>ICEM06

ICEM06 überprüft vom Modul auf ungültige direkte Verweise auf Features.

Mergemodul-ICEs werden in einer CUB-Mergemoduldatei namens Mergemod.cub und nicht in der CUB-Datei gespeichert, die die für die Paketvalidierung verwendeten ICEs enthält.

## <a name="result"></a>Ergebnis

ICEM06 gibt einen Fehler aus, wenn die Moduldatenbank direkte Verweise auf ein Feature enthält. Featureinformationen müssen vom Benutzer des Moduls bereitgestellt werden.

## <a name="example"></a>Beispiel

ICEM06 stellt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen zur Verfügung.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung          | Ziel                                 |
|-------------------|----------------------------------------|
| Shortcut1. *GUID1* | cmd.exe                                |
| Shortcut2. *GUID1* | \[MyProp\]                             |
| Shortcut3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Klassentabelle](class-table.md) (partiell)



| CLSID   | Kontext       | Komponente\_ | Komponente\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Komponente1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | MyFeature                              |



 

ICEM06 meldet den ersten Fehler, da der erste Datensatz in der Verknüpfungstabelle über einen Eintrag im Feld Ziel verfügt, der keine Eigenschaft oder NULL-GUID ist. Ein Modul kann nicht direkt auf ein Feature verweisen. Featureinformationen müssen vom Benutzer des Moduls bereitgestellt werden. Um diesen Fehler zu beheben, sollten Verweise auf ein Feature durch eine NULL-GUID ersetzt werden.

ICEM06 meldet den zweiten Fehler, da der zweite Datensatz in der Tabelle Klasse über einen Eintrag im Feld Feature verfügt, der keine NULL-GUID ist. Ein Modul kann nicht direkt auf ein Feature verweisen. Featureinformationen müssen vom Benutzer des Moduls bereitgestellt werden. Um diesen Fehler zu beheben, sollten Verweise auf ein Feature durch eine NULL-GUID ersetzt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Merge Module ICE Reference](merge-module-ice-reference.md)
</dt> </dl>

 

 



