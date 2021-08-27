---
title: FontSize-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die FontSize Commands-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cee9d4852a68792fe1270ebd9c91e51f567adc546433d7142de68392e9f8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751433"
---
# <a name="fontsize-property-commands-object"></a>FontSize-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Schriftgrad zurück, der im Popupmenü des Zeichens verwendet wird, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.FontSize-Punkte_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                              |
|----------|----------------------------------------------------------|
| *Punkte* | Ein ganzzahliger Wert vom Typ Long, der den Schriftgrad in Punkten angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **FontSize-Eigenschaft** definiert die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die **LanguageID-Einstellung** des Zeichens oder – wenn dies nicht festgelegt ist – auf der Standardspracheinstellung des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

 

 




