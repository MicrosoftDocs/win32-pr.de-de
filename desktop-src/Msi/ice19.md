---
description: ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KEYPATH-Spalte der Component-Tabelle verweisen und ob eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216745"
---
# <a name="ice19"></a>ICE19

ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KEYPATH-Spalte der [Component-Tabelle](component-table.md) verweisen und ob eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.

ICE19 überprüft, ob angekündigte Komponenten oder Verknüpfungen über eine ComponentID verfügen. Komponenten in der [PublishComponent-Tabelle](publishcomponent-table.md), die nicht in einer anderen Tabelle angekündigt werden, werden nur geprüft, um festzustellen, ob Sie über eine ComponentID verfügen.

## <a name="result"></a>Ergebnis

ICE19 gibt eine Fehlermeldung aus, wenn die KEYPATH-Spalte der Component-Tabelle nicht auf eine Datei im Fall einer angekündigten Komponente oder eines Verzeichnisses im Fall einer angekündigten Verknüpfung verweist. ICE19 gibt eine Fehlermeldung aus, wenn angekündigte Komponenten oder Verknüpfungen nicht über eine ComponentID verfügen.

## <a name="example"></a>Beispiel

ICE19 gibt die folgenden Fehlermeldungen für das gezeigte Beispiel aus:

-   Die Erweiterungs-FLP verweist auf die Komponente Comp1, die in der [Komponenten Tabelle](component-table.md)nicht über eine ComponentID verfügt.
-   Die Erweiterungs-exe verweist auf die Komponente Comp4, die auf ein Verzeichnis als KEYPATH verweist. Der KEYPATH ist in der Komponenten Tabelle NULL.
-   Verknüpfung Shortcut2 verweist auf die Komponente Comp3, die auf einen Registrierungs Eintrag als Schlüssel Pfad verweist. Der Wert der Spalte Attribute in der Komponenten Tabelle ist 4.

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente | ComponentID                            | Attribute | KEYPATH |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | Datei1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | Datei2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Erweiterungs Tabelle](extension-table.md) (partiell)



| Durchwahl | Komponente\_ |
|-----------|-------------|
| FLP       | Comp1       |
| TST       | Comp2       |
| exe       | Comp4       |



 

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Komponente\_ | Funktion\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | Productfeature |
| Shortcut2 | Comp3       | Productfeature |



 

[Funktions Tabelle](feature-table.md) (partiell)



| Funktion        |
|----------------|
| Productfeature |



 

> [!Note]  
> Wenn die Erweiterungs-FLP und die exe-Datei beide auf dieselbe Komponente verweisen, muss die exe-oder der com-Server, die Sie öffnet, identisch sein. Diese exe-Datei ist normalerweise der KEYPATH für die Komponente. Für Office können das Erweiterungs Dokument und XLS nicht auf dieselbe Komponente verweisen, da dieselbe exe nicht beide Erweiterungen öffnet. Sie müssen winword.exe, um doc-Erweiterungen zu öffnen, und Sie benötigen excel.exe, um XLS-Erweiterungen zu öffnen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



