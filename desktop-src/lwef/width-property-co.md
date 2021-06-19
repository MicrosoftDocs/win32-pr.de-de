---
title: Width-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Width-Eigenschaft des Characters-Objekts, die die Breite des Frames für das angegebene Zeichen zurückgibt oder legt.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395126"
---
# <a name="width-property-characters-object"></a>Width-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Breite des Frames für das angegebene Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Breitenwert_ *  \[ =  \]



| Teil    | Beschreibung                                                |
|---------|------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die die Framebreite des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**Width-Eigenschaft**](width-property.md) wird immer in Pixel ausgedrückt. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig angeordneten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.

 

 




