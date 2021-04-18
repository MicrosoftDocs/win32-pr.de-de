---
description: ICE76 überprüft die Verwendung des SFP (WFP)-Katalogs in Windows Installer Paketen für Windows Me. Dieses Eis überprüft auch, ob keine Dateien in der BindImage-Tabelle SFP-Kataloge referenzieren.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343347"
---
# <a name="ice76"></a>ICE76

ICE76 überprüft die Verwendung des SFP (WFP)-Katalogs in Windows Installer Paketen für Windows Me. Dieses Eis überprüft auch, ob keine Dateien in der BindImage- [Tabelle](bindimage-table.md) SFP-Kataloge referenzieren.

Der Windows-Datei Schutz erfordert eine genaue Entsprechung zwischen der Datei und der Signatur, die in die Katalog Datei eingebettet ist. Dateien, die auf einen SFP-Katalog verweisen, dürfen nicht in der Tabelle ' BindImage ' aufgeführt werden, da die Auswirkung der [BindImage-Aktion](bindimage-action.md) auf diese Dateien zwischen Computern abweicht. Dateien, auf die von SFP-Katalogen verwiesen wird, müssen in Komponenten vorliegen, die permanent sind oder lokal installiert sind

## <a name="result"></a>Ergebnis

ICE76 gibt einen Fehler für jede Datei in der [Tabelle BindImage](bindimage-table.md) aus, die auch in der [Tabelle filesfpcatalog](filesfpcatalog-table.md)vorliegt.

ICE76 gibt einen Fehler aus, wenn eine Datei in der filesfpcatalog-Tabelle zu einer Komponente mit einer der folgenden true gehört:

-   **msidbcomponentattributespermanent** ist nicht in der Attribute-Spalte der [Component-Tabelle](component-table.md)festgelegt.
-   **msidbcomponentattributessourceonly** wird in der Spalte Attribute der Komponenten Tabelle festgelegt.
-   **msidbattributesoptional** wird in der Spalte Attribute der Komponenten Tabelle festgelegt.

## <a name="example"></a>Beispiel

ICE76 meldet den folgenden Fehler für das Beispiel:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Filesfpcatalog-Tabelle](filesfpcatalog-table.md) (partiell)



| Datei\_ | Sfpcatalog\_ |
|--------|--------------|
| Datei1  | Catalog1.Cat |



 

[BindImage-Tabelle](bindimage-table.md) (partiell)



| Datei\_ |
|--------|
| Datei1  |



 

Um dieses Problem zu beheben, geben Sie keine Dateien ein, die auf SFP-Kataloge in der BindImage-Tabelle verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BindImage-Tabelle](bindimage-table.md)
</dt> <dt>

[Komponenten Tabelle](component-table.md)
</dt> <dt>

[Filesfpcatalog-Tabelle](filesfpcatalog-table.md)
</dt> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



