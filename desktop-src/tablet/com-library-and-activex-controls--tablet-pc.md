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
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="bbef9-103">COM-Bibliothek und ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="bbef9-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="bbef9-104">In diesem Abschnitt wird beschrieben, wie Sie Ihre Umgebung für die Verwendung der Tablet PC Platform-com-Bibliotheken in C++ einrichten.</span><span class="sxs-lookup"><span data-stu-id="bbef9-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="bbef9-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="bbef9-105">Microsoft Visual C++</span></span>

<span data-ttu-id="bbef9-106">Zum Erstellen von Tablet PC-Anwendungen in Visual C++ müssen Sie die System Umgebungsvariablen aktualisieren, Verzeichnis Optionen für Visual Studio einrichten und auf die Tablet PC-Schnittstellen in Ihrem Projekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="bbef9-107">Um die Umgebungsvariablen zu aktualisieren, befolgen Sie die Anweisungen des Windows SDK zum Hinzufügen der Umgebungsvariablen zu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bbef9-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="bbef9-108">Zugreifen auf die Tablet PC-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bbef9-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="bbef9-109">Für den Zugriff auf die Tablet PC-Schnittstellen müssen Sie die Dateien "msink AUT. h" und "msink AUT \_ i. c" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="bbef9-110">Sie können auch die folgende Import Direktive anstelle der \# zuvor aufgeführten include-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="bbef9-111">Für den Zugriff auf die InkAnalysis-Schnittstellen müssen Sie die Dateien "iacom. h" und "iacom \_ i. c" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="bbef9-112">Sie können auch die folgende Import Direktive anstelle der \# zuvor aufgeführten include-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="bbef9-113">Für den Zugriff auf die [**InkDivider**](inkdivider-class.md) -Schnittstellen müssen Sie msinkaut15 \_ i. c-und msinkaut15. h-Dateien in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="bbef9-114">InkDivider wurde durch die Ink-Analyse-APIs abgelöst.</span><span class="sxs-lookup"><span data-stu-id="bbef9-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="bbef9-115">Sie können auch die folgende Import Direktive anstelle der \# include-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="bbef9-116">Für den Zugriff auf die " [**pinputpanel**](peninputpanel-class.md) "-Schnittstellen müssen Sie die Dateien "pinputpanel \_ i. c" und "pinputpanel. h" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="bbef9-117">Sie können auch die folgende Import Direktive anstelle der \# include-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="bbef9-118">Die pinputpanel-APIs wurden in Windows Vista durch die neuen Text Eingabe Panel-Schnittstellen abgelöst.</span><span class="sxs-lookup"><span data-stu-id="bbef9-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="bbef9-119">Um auf die [InkEdit](inkedit-control-reference.md) -Steuerelement Schnittstellen zuzugreifen, müssen Sie die Dateien mit dem Dateiende ". h" und "eingebundene \_ i. c" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="bbef9-120">Alternativ können Sie \# die InkEd.dll Datei importieren.</span><span class="sxs-lookup"><span data-stu-id="bbef9-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



