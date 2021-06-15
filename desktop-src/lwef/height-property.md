---
title: Height-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die Height-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068510"
---
# <a name="height-property-characters-object"></a>Height-Eigenschaft (Characters-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Höhe des Rahmens des angegebenen Zeichens zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ *  \[ =  *Height-Wert*\]



| Teil    | Beschreibung                                                 |
|---------|-------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die die Framehöhe des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Height-Eigenschaft** wird immer in Pixeln relativ zu Bildschirmkoordinaten (oben links) ausgedrückt. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig gestalteten Bereichsfenster angezeigt wird, basiert die Höhe des Zeichens auf den externen Dimensionen des rechteckigen Animationsframes, der beim Kompilieren des Zeichens mit dem Microsoft Agent-Zeichen-Editor verwendet wurde.

 

 




