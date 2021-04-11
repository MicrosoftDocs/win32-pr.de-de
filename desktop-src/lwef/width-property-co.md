---
title: Width-Eigenschaft (Character-Objekt)
description: Width-Eigenschaft
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039958"
---
# <a name="width-property-characters-object"></a>Width-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Breite des Frames für das angegebene Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Width_- *  \[ =  *Wert*\]



| Teil    | BESCHREIBUNG                                                |
|---------|------------------------------------------------------------|
| *value* | Eine lange ganze Zahl, die die Rahmenbreite des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**Width**](width-property.md) -Eigenschaft wird immer in Pixel ausgedrückt. Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf den externen Dimensionen des rechteckigen Animations Rahmens, der verwendet wurde, als das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wurde.

 

 




