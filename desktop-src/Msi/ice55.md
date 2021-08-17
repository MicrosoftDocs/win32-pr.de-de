---
description: ICE55 überprüft, ob alle LockPermission-Objekte vorhanden sind und gültige Berechtigungswerte aufweisen.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044b9993c6c50dce32c04f98d8e000f0faae4280d244c4656d7b0cbed7b49749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635141"
---
# <a name="ice55"></a>ICE55

ICE55 überprüft, ob alle LockPermission-Objekte vorhanden sind und gültige Berechtigungswerte aufweisen.

## <a name="result"></a>Ergebnis

ICE55 post an error if a LockObject listed in the LockPermissions table does not exist or if no privilege level is specified in the Permission column. (ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.

## <a name="example"></a>Beispiel

ICE55 meldet die folgenden Fehler für das Beispiel.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[LockPermissions-Tabelle](lockpermissions-table.md) (partiell)



| LockObject | Tabelle | Domain | Benutzer  | Berechtigung |
|------------|-------|--------|-------|------------|
| Datei1      | Datei  |        | guest |            |
| Datei3      | Datei  |        | guest | 1          |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Version | Sprache |
|-------|---------|----------|
| Datei1 | Datei2   |          |
| Datei2 | 1.0.0.0 | 1033     |



 

Das Objekt File1 weist in der Spalte Permission einen NULL-Wert auf. Jede Zeile muss einen Wert in der Spalte Berechtigungen aufweisen. Um diesen Fehler zu beheben, geben Sie einen numerischen Wert in dieser Spalte an. Wenn für dieses Objekt keine Berechtigungen erforderlich sind, sollten Sie die Zeile entfernen.

Das in der LockPermissions-Tabelle beschriebene File3-Objekt ist nicht in der Dateitabelle aufgeführt. Um diesen Fehler zu beheben, verweisen Sie auf ein gültiges -Objekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



