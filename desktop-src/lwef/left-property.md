---
title: Left-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Left Characters-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988936"
---
# <a name="left-property-characters-object"></a>Left-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den linken Rand des Rahmens des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Linker_ *  \[  =  *Wert*\]



| Teil    | Beschreibung                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die den linken Rand des Rahmens des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Left-Eigenschaft** wird immer in Pixel ausgedrückt, relativ zum Ursprung des Bildschirms (links oben). Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig angeordneten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.

 

 




