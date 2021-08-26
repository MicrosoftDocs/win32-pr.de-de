---
description: Stellt Informationen zu einem Experiment (Erfassung) dar.
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Experimentstruktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ebe9ab0232104886078256effdfaf5534144dc30421dab2ac2359ef390c0a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118150"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Experimentstruktur

Stellt Informationen zu einem Experiment (Erfassung) dar.

## <a name="syntax"></a>Syntax


```C++
} Experiment;
```

## <a name="members"></a>Member

**Processid**  
Die zugeordnete Prozess-ID.

**applicationName**  
Eine COM-Zeichenfolge, die den Namen der Anwendung enthält, für die das Experiment ausgeführt werden soll.

**commandLineArguments**  
Eine COM-Zeichenfolge, die die Befehlszeilenargumente enthält.

**workingDirectory**  
Eine COM-Zeichenfolge, die den Pfad des Arbeitsverzeichnisses enthält.

**tempPixRunFile**  
Eine COM-Zeichenfolge, die den Dateipfad der temporären Datei enthält, die zum Ausführen des Experiments verwendet wird.

**startOption**  
Die dem Experiment zugeordnete Startoption.

**experimentType**  
Die Art des Experiments (Erfassung).

**uiLocale**  
Die ID des Gebietsschemas, das während der Erfassung für UI-Überlagerungselemente verwendet wird. Dies wird vom Host (z. B. Visual Studio Grafikdiagnose) an die Erfassungs-Engine übergeben.

**registryRoot**  
Eine COM-Zeichenfolge, die den Registrierungsstamm enthält. Dies wird vom Host (z. B. Visual Studio Grafikdiagnose) an die Erfassungs-Engine übergeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



