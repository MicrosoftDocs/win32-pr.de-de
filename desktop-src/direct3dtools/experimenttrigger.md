---
description: Stellt Experiment auslöserinformationen dar.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Experiment auslöst-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860214"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span id="vspixengine.experimenttrigger"></span>Experiment auslöst-Struktur

Stellt Experiment auslöserinformationen dar.

## <a name="syntax"></a>Syntax


```C++
} ExperimentTrigger;
```

## <a name="members"></a>Member

**type**  
Die Art von Experiment (Erfassung), die ausgelöst wurde.

**key**  
Wenn Type dem Typ experimenttriggertype:: Key entspricht, wird der Schlüssel verwendet, um die Erfassung zu initiieren.

**Framezahl**  
Wenn Type dem Typ experimenttriggertype:: framenumber entspricht, wird die Frame Nummer, die die Erfassung auslöst, ausgelöst.

**capturecount**  
Die Anzahl der zu erfassenden sequenziellen Frames.

**Aktions-ID**  
Die ID des Aktions Ereignisses (Screenshot, Frame Erfassung usw.).

**Action playload**  
Ein Zeiger auf die Nutzlast des Aktions Ereignisses.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



