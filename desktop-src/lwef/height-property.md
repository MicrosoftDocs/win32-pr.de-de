---
title: Height-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Height-Eigenschaft des Characters-Objekts. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ecd8e48b63a426ec8508f3838ec9f9dc24ebd6289f9482ab796bb22e388e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693406"
---
# <a name="height-property-characters-object"></a>Height-Eigenschaft (Characters-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Höhe des Rahmens des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Höhenwert_ *  \[ =  \]



| Teil    | Beschreibung                                                 |
|---------|-------------------------------------------------------------|
| *value* | Eine long-Ganzzahl, die die Framehöhe des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Height-Eigenschaft** wird immer in Pixel ausgedrückt, relativ zu Bildschirmkoordinaten (oben links). Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierten Bereichsfenster angezeigt wird, basiert die Höhe des Zeichens auf den externen Abmessungen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft-Agent-Zeichen-Editor verwendet wurde.

 

 




