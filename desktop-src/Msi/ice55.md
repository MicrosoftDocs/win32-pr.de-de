---
description: ICE55 überprüft, ob alle lockberechtigungsobjekte vorhanden sind und gültige Berechtigungs Werte aufweisen.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217352"
---
# <a name="ice55"></a>ICE55

ICE55 überprüft, ob alle lockberechtigungsobjekte vorhanden sind und gültige Berechtigungs Werte aufweisen.

## <a name="result"></a>Ergebnis

ICE55 Posten Sie einen Fehler, wenn ein in der [lockberechtigungstabelle](lockpermissions-table.md) aufgelistetes lockobject-Objekt nicht vorhanden ist oder wenn keine Berechtigungsebene in der Berechtigungs Spalte angegeben ist.

## <a name="example"></a>Beispiel

ICE55 würde die folgenden Fehler für das Beispiel melden.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Lockberechtigungs Tabelle](lockpermissions-table.md) (partiell)



| LockObject | Tabelle | Domain | Benutzer  | Berechtigung |
|------------|-------|--------|-------|------------|
| Datei1      | File  |        | guest |            |
| Datei3      | File  |        | guest | 1          |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Version | Sprache |
|-------|---------|----------|
| Datei1 | Datei2   |          |
| Datei2 | 1.0.0.0 | 1033     |



 

Das Objekt file1 weist in der Berechtigungs Spalte den Wert NULL auf. Jede Zeile muss über einen Wert in der Spalte "Berechtigungen" verfügen. Um diesen Fehler zu beheben, geben Sie einen numerischen Wert in dieser Spalte an. Wenn für dieses Objekt keine Berechtigungen erforderlich sind, sollten Sie die Zeile entfernen.

Das in der lockberechtigungs-Tabelle beschriebene Objekt datei3 ist in der Dateitabelle nicht aufgeführt. Um diesen Fehler zu beheben, verweisen Sie auf ein gültiges-Objekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



