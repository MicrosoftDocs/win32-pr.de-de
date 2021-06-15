---
title: FontSize-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die FontSize Balloon-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068217"
---
# <a name="fontsize-property-balloon-object"></a>FontSize-Eigenschaft (Balloon-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Schriftgrad zurück, der für das Wort balloon für das angegebene Zeichen unterstützt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.**Characters* *  **("**_CharacterID_*_"). Balloon.FontSize-Punkte_* \[  =  \]



| Teil     | Beschreibung                                              |
|----------|----------------------------------------------------------|
| *Punkte* | Ein ganzzahliger Long-Wert, der den Schriftgrad in Punkten angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**FontSize-Eigenschaft**](fontsize-property.md) gibt einen long integer-Wert zurück, der den aktuellen Schriftgrad in Punkten angibt. Der Höchstwert für **FontSize** beträgt 2160 Punkte.

Der Standardwert für die Schriftarteinstellungen der Wortsprechblase eines Zeichens wird im Microsoft Agent-Zeichen-Editor festgelegt. Darüber hinaus kann der Benutzer Schriftarteinstellungen für alle Zeichen im Microsoft Agent-Eigenschaftenblatt überschreiben.

 

 




