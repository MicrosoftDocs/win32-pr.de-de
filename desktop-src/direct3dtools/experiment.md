---
description: Stellt Informationen zu einem Experiment (Erfassung) dar.
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Experiment Struktur
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
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746441"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Experiment Struktur

Stellt Informationen zu einem Experiment (Erfassung) dar.

## <a name="syntax"></a>Syntax


```C++
} Experiment;
```

## <a name="members"></a>Member

**ProcessID**  
Die zugeordnete Prozess-ID.

**applicationName**  
Eine com-Zeichenfolge mit dem Namen der Anwendung, für die das Experiment ausgeführt werden soll.

**commandLineArguments**  
Eine com-Zeichenfolge, die die Befehlszeilenargumente enthält.

**workingDirectory**  
Eine com-Zeichenfolge, die den Pfad des Arbeitsverzeichnisses enthält.

**temppixrunfile**  
Eine com-Zeichenfolge, die den filePath der zum Ausführen des Experiments verwendeten temporären Datei enthält.

**Startoption**  
Die dem Experiment zugeordnete Startoption.

**experimentstyp**  
Die Art des Experiments (Erfassung).

**uilocale**  
Die ID des Gebiets Schemas, das während der Überlagerung (Erfassung) für UI-Überlagerungs Elemente verwendet wird. Diese wird vom Host (z. b. Visual Studio Grafikdiagnose) an die Aufzeichnungs-Engine übermittelt.

**registryRoot**  
Eine com-Zeichenfolge, die den Registrierungs Stamm enthält. Diese wird vom Host (z. b. Visual Studio Grafikdiagnose) an die Aufzeichnungs-Engine übermittelt.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



