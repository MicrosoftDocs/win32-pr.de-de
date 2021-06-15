---
title: FontName-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die FontName Commands-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068256"
---
# <a name="fontname-property-commands-object"></a>FontName-Eigenschaft (Commands-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Schriftart zurück, die im Popupmenü des Zeichens verwendet wird, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.FontName-Schriftart_ *  \[  =  \]



| Teil   | Beschreibung                                      |
|--------|--------------------------------------------------|
| *Schriftart* | Ein Zeichenfolgenwert, der dem Namen der Schriftart entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **FontName-Eigenschaft** definiert die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die **LanguageID-Einstellung** des Zeichens oder – wenn dies nicht festgelegt ist – der Standardeinstellung für die Sprach-ID des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

 

 




