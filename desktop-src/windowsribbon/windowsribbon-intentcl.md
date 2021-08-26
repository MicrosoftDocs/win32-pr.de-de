---
title: Kompilieren von Menübandmarkup
description: Damit das Windows Menübandframework die Menüband-Markupdatei nutzen kann, muss die Markupdatei in eine Ressourcendatei im Binärformat kompiliert werden.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows Menüband,Kompilieren von Markup
- Menüband,Kompilieren von Markup
- Windows Menüband, Compilerworkflow
- Menüband, Compilerworkflow
- Windows Menüband, UI-Befehlscompiler (UICC.exe)
- Menüband, UI-Befehlscompiler (UICC.exe)
- UI-Befehlscompiler (UICC.exe)
- UICC.exe (UI-Befehlscompiler)
- Kompilieren Windows Menübandmarkups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefd64103ceb501e8f4d23e937a242e910b0cad5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884904"
---
# <a name="compiling-ribbon-markup"></a>Kompilieren von Menübandmarkup

Damit das Windows Menübandframework die [Menüband-Markupdatei](windowsribbon-schema.md) nutzen kann, muss die Markupdatei in eine Binärformatressourcendatei kompiliert werden. Ein dedizierter Markupcompiler, der UICC (UI Command Compiler), ist zu diesem Zweck im Windows Software Development Kit (SDK) (7.0 oder höher) enthalten. Zusätzlich zum Kompilieren der binären Version des Markups generiert UICC eine ID-Definitionsheaderdatei (.h), die alle Markupelemente für die Menübandhostanwendung und eine Ressourcendatei (RC) verfügbar macht, mit der Image- und Zeichenfolgenressourcen zur Buildzeit mit der Hostanwendung verknüpft werden.

-   [Compilerworkflow](#compiler-workflow)
-   [Befehlszeilensyntax](#command-line-syntax)
    -   [Argumente und Optionen](#arguments-and-options)
    -   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="compiler-workflow"></a>Compilerworkflow

Der Workflow des Menübandmarkupcompiler wird im folgenden Diagramm veranschaulicht.

![Diagramm, das den Workflow des Menübandmarkupcompiler zeigt.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die Befehlszeilensyntax für den Menübandmarkupcompiler wird im folgenden Beispiel gezeigt.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumente und Optionen

Die Argumente und Optionen für dieses Tool werden in der folgenden Tabelle beschrieben.

> [!Note]  
> Die aufgeführten Befehlszeilenoptionen müssen in der angegebenen Reihenfolge angegeben werden.

 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/header: &lt; headerFile&gt;</td>
<td>Generieren Sie eine Headerdatei namens &lt; &gt; headerFile, die die Ressourcensymbole der Markupbefehls-ID enthält. Wenn sie nicht angegeben wird, wird keine Headerdatei generiert.</td>
</tr>
<tr class="even">
<td>/res:<resourceFile></td>
<td>Generieren Sie eine Ressourcendatei namens <resourceFile> , die alle Bild- und Zeichenfolgenressourcen, die binäre Markupdatei und die Headerdatei zur Buildzeit mit der Hostanwendung verknüpft. Wenn keine Angabe erfolgt, wird keine Ressourcendatei generiert.</td>
</tr>
<tr class="odd">
<td>/name:<ribbonName></td>
<td>Der Ressourcenname für die binäre Markupdatei, die im protokolliert <resourceFile> wird. Der Standardwert ist APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtern Sie die Ereignismeldungen nach Schweregrad. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Nur Fehlermeldungen.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Nur Fehler- und Warnmeldungen.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Standard. <br/> Fehler-, Warnungs- und Informationsmeldungen.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie der Menübandmarkupcompiler verwendet wird, um einen typischen Satz von Ressourcendateien für eine Menübandanwendung zu generieren.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](windowsribbon-schema.md)
</dt> <dt>

[Erstellen einer Menübandanwendung](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





