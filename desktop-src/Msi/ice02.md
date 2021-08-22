---
description: ICE02 überprüft, ob bestimmte Verweise zwischen den Tabellen Component, File und Registry reziprok sind. Diese Verweise müssen reziprok sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen kann.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97696ee4a8f93d49237dbac8661b6bfc72e478922c87b9095620bc5c29dc546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946654"
---
# <a name="ice02"></a>ICE02

ICE02 überprüft, ob bestimmte Verweise zwischen den Tabellen [Component,](component-table.md) [File](file-table.md)und [Registry](registry-table.md) reziprok sind. Diese Verweise müssen reziprok sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen kann.

Das Installationsprogramm verwendet die KeyPath-Spalte der Component -Tabelle, um das Vorhandensein der komponente zu erkennen, die in der Spalte Komponente aufgeführt ist. Die KeyPath -Spalte enthält einen Schlüssel in der Registrierungs- oder Dateitabelle. Beide Tabellen verfügen über eine Component-Spalte, die einen Schlüssel zurück in die Component-Tabelle enthält, der auf die Komponente zeigt, die den Registrierungseintrag oder die \_ Datei steuert. Diese Verweise müssen reziprok sein.

## <a name="result"></a>Ergebnis

ICE02 gibt eine Fehlermeldung aus, wenn ein Verweis gefunden wird, der reziprok sein sollte und nicht ist.

## <a name="example"></a>Beispiel

ICE02 würde die folgende Fehlermeldung für eine Datei .msi, die die angezeigten Datenbankeinträge enthält.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Komponententabelle](component-table.md) (partiell)



| Komponente | KeyPath   |
|-----------|-----------|
| Red       | Rote \_ Datei |
| Blau      | Rote \_ Datei |



 

[Dateitabelle](file-table.md) (partiell)



| Dateispalte | Komponente\_ |
|-------------|-------------|
| Rote \_ Datei   | Red         |
| Blaue \_ Datei  | Blau        |



 

Component Blue verweist auf Red File, aber Red File wird nicht von Component Blue gesteuert und kann daher nicht \_ \_ die KeyPath-Datei sein. Wenn das Installationsprogramm aufgerufen wird, um den Installationsstatus Blau zu erhalten, wird fälschlicherweise überprüft, ob die \_ rote Datei installiert wurde. Wenn Sie das Feld KeyPath für Blau in der Komponententabelle in Blaue Datei ändern, \_ wird der Fehler behoben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



