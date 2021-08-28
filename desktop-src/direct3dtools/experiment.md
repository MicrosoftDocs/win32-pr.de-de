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
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625366"
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
Eine COM-Zeichenfolge, die den Namen der Anwendung enthält, auf der das Experiment ausgeführt werden soll.

**commandLineArguments**  
Eine COM-Zeichenfolge, die die Befehlszeilenargumente enthält.

**workingDirectory**  
Eine COM-Zeichenfolge, die den Pfad des Arbeitsverzeichnisses enthält.

**tempPixRunFile**  
Eine COM-Zeichenfolge, die den Dateipfad der temporären Datei enthält, die zum Ausführen des Experiments verwendet wird.

**startOption**  
Die start-Option, die dem Experiment zugeordnet ist.

**experimentType**  
Die Art des Experiments (Erfassung).

**uiLocale**  
Die ID des Für benutzeroberflächenüberlagerungselemente während der Auslösung (Erfassung) verwendeten Locales. Diese wird vom Host (z. B. Visual Studio Grafikdiagnose) an die Erfassungs-Engine übergeben.

**registryRoot**  
Eine COM-Zeichenfolge, die den Registrierungsstamm enthält. Diese wird vom Host (z. B. Visual Studio Grafikdiagnose) an die Erfassungs-Engine übergeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



