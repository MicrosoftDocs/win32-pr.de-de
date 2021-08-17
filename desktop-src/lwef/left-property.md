---
title: Left-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Left Characters-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105016"
---
# <a name="left-property-characters-object"></a>Left-Eigenschaft (Characters-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den linken Rand des Frames des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Linker_ *  \[  =  *Wert*\]



| Teil    | BESCHREIBUNG                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Eine long-Ganzzahl, die den linken Rand des Rahmens des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Left-Eigenschaft** wird immer in Pixel ausgedrückt, relativ zum Bildschirmursprung (oben links). Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft-Agent-Zeichen-Editor verwendet wurde.

 

 




