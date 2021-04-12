---
description: ICE40 führt verschiedene Überprüfungen durch.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131872"
---
# <a name="ice40"></a>ICE40

ICE40 führt verschiedene Überprüfungen durch.

## <a name="result"></a>Ergebnis

ICE40 gibt Warnungen zu folgenden Aktionen aus:

-   Die Eigenschaft " [**REINSTALLMODE**](reinstallmode.md) " wurde überschrieben.
-   Die [removeinifile-Tabelle](removeinifile-table.md) enthält einen DELETE-tageintrag ohne Wert.
-   In der MSI-Datei fehlt die [Fehler Tabelle](error-table.md) , und die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) ist kleiner oder gleich 100. Diese Ice-Warnung ist veraltet, da Windows Installer nicht erfordert, dass das Paket eine Fehler Tabelle enthält. Fehlermeldungen können mit Msimsg.dll abgerufen werden.

## <a name="example"></a>Beispiel

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft                               | Wert |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | A     |



 

[Removeinifile-Tabelle](removeinifile-table.md)



| Removeinifile                          | Aktion | Wert |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Ergebnisse

ICE40 würde die folgenden Fehler melden.



| ICE40-Fehler                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) ist in der Eigenschaften Tabelle definiert. Dies kann zu Problemen führen. | Das Definieren der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft in der MSI-Datei kann zu unerwartetem Verhalten führen. Legen Sie diese Eigenschaft nicht fest, um diesen Fehler zu beheben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Der removeinifile-Eintrag Remove1 muss über einen Wert verfügen, da die Aktion "Delete Tag" (4) ist.                | In der removeinifile-Spalte der [removeinifile-Tabelle](removeinifile-table.md) ist eine DELETE-tagaktion vorhanden, ohne dass ein zu löschende Tag in der Spalte Wert angegeben werden muss.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Fehler Tabelle fehlt. Nur numerische Fehlermeldungen werden generiert.                              | Diese Ice-Warnung ist veraltet, da Windows Installer nicht erfordert, dass das Paket eine [Fehler Tabelle](error-table.md)enthält. Fehlermeldungen können mit Msimsg.dll abgerufen werden.<br/> Diese Warnung bedeutet, dass in der MSI-Datei die [Fehler Tabelle](error-table.md) fehlt und die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) kleiner oder gleich 100 ist. <br/> Um diesen Fehler zu beheben, verwenden Sie eine aktuelle Version der Windows Installer, oder fügen Sie dem Installationspaket eine Fehler Tabelle hinzu, und erstellen Sie Formatierungs Vorlagen in der Meldungs Spalte für Fehlermeldungen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




