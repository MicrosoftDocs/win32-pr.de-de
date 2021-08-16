---
title: Top-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Top-Eigenschaft (Characters-Objekt). Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bdc753bc287e1289b2a75633081c7b325d698a7fbe92ba495cc93662485d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474478"
---
# <a name="top-property-characters-object"></a>Top-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den oberen Rand des Rahmens des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Oberster_ *  \[  =  *Wert*\]



| Teil    | BESCHREIBUNG                                             |
|---------|---------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die den oberen Rand des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Top-Eigenschaft** wird immer in Pixel ausgedrückt, relativ zum Ursprung des Bildschirms (links oben). Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig angeordneten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.

Verwenden Sie [**die MoveTo-Methode,**](moveto-method.md) um die Position des Zeichens zu ändern.

## <a name="see-also"></a>Weitere Informationen

[**Left-Eigenschaft,**](left-property.md) [ **MoveTo-Methode**](moveto-method.md)


 

 




