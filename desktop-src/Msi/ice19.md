---
description: ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KeyPath-Spalte der Component-Tabelle verweisen und dass eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1a706999744762a930a800326cb8d38487f19c1c4ea3e01b6b1f8aeae4ca2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529110"
---
# <a name="ice19"></a>ICE19

ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KeyPath-Spalte der [Component-Tabelle](component-table.md) verweisen und dass eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.

ICE19 überprüft, ob angekündigte Komponenten oder Verknüpfungen über eine ComponentId verfügen. Komponenten in der [PublishComponent-Tabelle,](publishcomponent-table.md)die nicht in einer anderen Tabelle angekündigt werden, werden nur überprüft, um festzustellen, ob sie über eine ComponentId verfügen.

## <a name="result"></a>Ergebnis

ICE19 gibt eine Fehlermeldung aus, wenn die KeyPath-Spalte der Tabelle Komponente im Fall einer angekündigten Komponente oder eines Verzeichnisses im Fall einer angekündigten Verknüpfung nicht auf eine Datei verweist. ICE19 sendet eine Fehlermeldung, wenn angekündigte Komponenten oder Verknüpfungen keine ComponentId aufweisen.

## <a name="example"></a>Beispiel

ICE19 sendet die folgenden Fehlermeldungen für das gezeigte Beispiel:

-   Extension flp verweist auf die Komponente Comp1, für die in der [Tabelle Component](component-table.md)keine ComponentId angegeben ist.
-   Extension exe verweist auf die Komponente Comp4, die auf ein Verzeichnis als KeyPath verweist. KeyPath ist in der Component-Tabelle NULL.
-   Shortcut2 verweist auf die Komponente Comp3, die auf einen Registrierungseintrag als Schlüsselpfad verweist. Der Wert der Attributes -Spalte in der Component-Tabelle ist 4.

[Komponententabelle](component-table.md) (teilweise)



| Komponente | Componentid                            | Attribute | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | Datei1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | Datei2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Erweiterungstabelle](extension-table.md) (teilweise)



| Erweiterung | Komponente\_ |
|-----------|-------------|
| Flp       | Comp1       |
| Tst       | Comp2       |
| exe       | Comp4       |



 

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Komponente\_ | Feature\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | Comp3       | ProductFeature |



 

[Featuretabelle](feature-table.md) (teilweise)



| Feature        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Wenn die Erweiterung flp und exe auf dieselbe Komponente verweisen, muss der EXE- oder COM-Server, der sie öffnet, identisch sein. Diese EXE ist normalerweise der KeyPath für die Komponente. Für OFFICE können die Erweiterungen doc und xls nicht auf dieselbe Komponente verweisen, da die gleiche EXE nicht beide Erweiterungen öffnet. Sie benötigen winword.exe, um Doc-Erweiterungen zu öffnen, und Sie benötigen excel.exe, um XLS-Erweiterungen zu öffnen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



