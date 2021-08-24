---
title: FontName-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die FontName Commands-Objekteigenschaft. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1f8c9c66e7d205e79a3ac9b076fa4e01852df358657761f8792d42b764b270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725710"
---
# <a name="fontname-property-commands-object"></a>FontName-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die schriftart zurück, die im Popupmenü des Zeichens verwendet wird, oder legt sie fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_")._ *  \[  =  *Commands.FontName-Schriftart*\]



| Teil   | Beschreibung                                      |
|--------|--------------------------------------------------|
| *Schriftart* | Ein Zeichenfolgenwert, der dem Namen der Schriftart entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **FontName-Eigenschaft** definiert die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die **LanguageID-Einstellung** des Zeichens oder auf der Einstellung für die Standardsprach-ID des Benutzers, wenn dies nicht festgelegt ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

 

 




