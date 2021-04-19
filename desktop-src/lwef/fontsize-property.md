---
title: FontSize-Eigenschaft (Commands-Objekt)
description: FontSize-Eigenschaft
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337892"
---
# <a name="fontsize-property-commands-object"></a>FontSize-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Schrift Grad zurück, der im Popupmenü des Zeichens verwendet wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Commands. FontSize_- *  \[  =  *Punkte*\]



| Teil     | BESCHREIBUNG                                              |
|----------|----------------------------------------------------------|
| *Punkt* | Ein Long Integer-Wert, der den Schrift Grad in Punkten angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **FontSize** -Eigenschaft definiert die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung der Schriftart für die **LanguageID** -Einstellung des Zeichens oder –, wenn dies nicht festgelegt ist – der Standard Spracheinstellung des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

 

 




