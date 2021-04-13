---
title: Page-Eigenschaft
description: Page-Eigenschaft
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388291"
---
# <a name="page-property"></a>Page-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die im Eigenschaften Blatt des Microsoft-Agents angezeigte Seite zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax** 
</dt> <dd>

*Agent * * *. PropertySheet.Page*- *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck mit einem der folgenden Werte. **"Sprache"** Zeigt die Seite für die Spracheingabe an.<br/> **"Ausgabe"** Zeigt die Ausgabe Seite an.<br/> **"Copyright"** Zeigt die Copyright Seite an.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn keine Sprach-Engine installiert ist, hat das Festlegen der **Seite** auf **"Speech"** keine Auswirkung. Außerdem muss die **sichtbare** Eigenschaft des Fensters auf **true** festgelegt werden, damit der Benutzer die Seite sehen kann.

> [!Note]  
> Der Benutzer kann diese Eigenschaft überschreiben.

 

 

 





