---
title: Top-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Top-Eigenschaft (Characters-Objekt). Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396345"
---
# <a name="top-property-characters-object"></a>Top-Eigenschaft (Characters-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den oberen Rand des Rahmens des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Oberster_ *  \[  =  *Wert*\]



| Teil    | Beschreibung                                             |
|---------|---------------------------------------------------------|
| *value* | Eine long-Ganzzahl, die den oberen Rand des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Top-Eigenschaft** wird immer in Pixel relativ zum Bildschirmursprung (oben links) ausgedrückt. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsrahmens, der beim Kompilieren des Zeichens mit dem Microsoft-Agent-Zeichen-Editor verwendet wurde.

Verwenden Sie die [**MoveTo-Methode,**](moveto-method.md) um die Position des Zeichens zu ändern.

## <a name="see-also"></a>Weitere Informationen

[**Left-Eigenschaft,**](left-property.md) [ **MoveTo-Methode**](moveto-method.md)


 

 




