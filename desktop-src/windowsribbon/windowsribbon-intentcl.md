---
title: Kompilieren von Menü Band Markup
description: Damit das Windows-Menüband-Framework die Menüband-Markup Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows-Menüband, Kompilieren von Markup
- Menüband, Kompilieren von Markup
- Windows-Multifunktionsleiste, compilerworkflow
- Multifunktionsleiste, compilerworkflow
- Windows-Menüband, UI-Befehls Compiler (UICC.exe)
- Multifunktionsleiste, UI-Befehls Compiler (UICC.exe)
- UI-Befehls Compiler (UICC.exe)
- UICC.exe (UI-Befehls Compiler)
- Kompilieren von Windows-Menü Band Markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515950"
---
# <a name="compiling-ribbon-markup"></a>Kompilieren von Menü Band Markup

Damit das Windows-Menüband-Framework die [Menüband-Markup](windowsribbon-schema.md) Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden. Ein dedizierter Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Windows Software Development Kit (SDK) (7,0 oder höher) enthalten. Zusätzlich zum Kompilieren der Binärversion des Markups generiert das UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) verfügbar macht, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.

-   [Compilerworkflow](#compiler-workflow)
-   [Befehlszeilen Syntax](#command-line-syntax)
    -   [Argumente und Optionen](#arguments-and-options)
    -   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="compiler-workflow"></a>Compilerworkflow

Der Workflow des Menüband-Markup Compilers ist im folgenden Diagramm dargestellt.

![Diagramm mit dem Workflow für den Menüband-Markup Compiler.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Das folgende Beispiel zeigt die Befehlszeilen Syntax für den Menüband-Markup Compiler.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumente und Optionen

Die Argumente und Optionen für dieses Tool werden in der folgenden Tabelle beschrieben.

> [!Note]  
> Die aufgelisteten Befehlszeilenoptionen müssen in der angegebenen Reihenfolge angegeben werden.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/Header<headerFile></td>
<td>Generieren Sie eine Header Datei mit <headerFile> dem Namen, die die Markup Befehls-ID-Ressourcen Symbole enthält. Wenn der Wert nicht weggelassen wird, wird keine Header Datei generiert.</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>Generieren Sie eine Ressourcen Datei <resourceFile> mit dem Namen, die alle Bild-und Zeichen folgen Ressourcen, die binäre Markup Datei und die Header Datei zur Buildzeit mit der Host Anwendung verknüpft. Wenn der Wert nicht weggelassen wird, wird keine Ressourcen Datei generiert.</td>
</tr>
<tr class="odd">
<td>/Name<ribbonName></td>
<td>Der Ressourcen Name für die binäre Markup Datei, die in protokolliert wird <resourceFile> . Der Standardwert ist APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtern Sie die Ereignismeldungen basierend auf dem Schweregrad. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Nur Fehlermeldungen.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Nur Fehler-und Warnmeldungen.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Standard. <br/> Fehler-, Warn-und Informationsmeldungen.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie der multifunktionsleistenmarkup-Compiler verwendet wird, um einen typischen Satz von Ressourcen Dateien für eine Multifunktionsleistenanwendung zu generieren.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)
</dt> <dt>

[Erstellen einer Menü Bandanwendung](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





