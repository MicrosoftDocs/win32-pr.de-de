---
description: In diesem Abschnitt wird beschrieben, wie Sie Ihre Umgebung für die Verwendung der Tablet PC Platform-com-Bibliotheken in C++ einrichten.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: COM-Bibliothek und ActiveX-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345468"
---
# <a name="com-library-and-activex-controls"></a>COM-Bibliothek und ActiveX-Steuerelemente

In diesem Abschnitt wird beschrieben, wie Sie Ihre Umgebung für die Verwendung der Tablet PC Platform-com-Bibliotheken in C++ einrichten.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Zum Erstellen von Tablet PC-Anwendungen in Visual C++ müssen Sie die System Umgebungsvariablen aktualisieren, Verzeichnis Optionen für Visual Studio einrichten und auf die Tablet PC-Schnittstellen in Ihrem Projekt zugreifen.

Um die Umgebungsvariablen zu aktualisieren, befolgen Sie die Anweisungen des Windows SDK zum Hinzufügen der Umgebungsvariablen zu Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Zugreifen auf die Tablet PC-Schnittstellen

Für den Zugriff auf die Tablet PC-Schnittstellen müssen Sie die Dateien "msink AUT. h" und "msink AUT \_ i. c" in Ihr Projekt einschließen.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Sie können auch die folgende Import Direktive anstelle der \# zuvor aufgeführten include-Anweisungen verwenden.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Für den Zugriff auf die InkAnalysis-Schnittstellen müssen Sie die Dateien "iacom. h" und "iacom \_ i. c" in Ihr Projekt einschließen.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



Sie können auch die folgende Import Direktive anstelle der \# zuvor aufgeführten include-Anweisungen verwenden.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Für den Zugriff auf die [**InkDivider**](inkdivider-class.md) -Schnittstellen müssen Sie msinkaut15 \_ i. c-und msinkaut15. h-Dateien in Ihr Projekt einschließen.

> [!Note]  
> InkDivider wurde durch die Ink-Analyse-APIs abgelöst.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



Sie können auch die folgende Import Direktive anstelle der \# include-Anweisungen verwenden.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Für den Zugriff auf die " [**pinputpanel**](peninputpanel-class.md) "-Schnittstellen müssen Sie die Dateien "pinputpanel \_ i. c" und "pinputpanel. h" in Ihr Projekt einschließen.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



Sie können auch die folgende Import Direktive anstelle der \# include-Anweisungen verwenden.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> Die pinputpanel-APIs wurden in Windows Vista durch die neuen Text Eingabe Panel-Schnittstellen abgelöst.

 

Um auf die [InkEdit](inkedit-control-reference.md) -Steuerelement Schnittstellen zuzugreifen, müssen Sie die Dateien mit dem Dateiende ". h" und "eingebundene \_ i. c" in Ihr Projekt einschließen.


```C++
#include <inked.h>
#include <inked_i.c>
```



Alternativ können Sie \# die InkEd.dll Datei importieren.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



