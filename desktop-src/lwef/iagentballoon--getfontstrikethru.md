---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b15bfbc120f7c8d614839f55ec985a3bdbdb3f840e5a07d615f7de0dfc75e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751024"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Gibt an, ob für die in einem Wortsprechblasen verwendete Schriftart der durchgestrichene Stil festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

Die Adresse eines Werts, der **True** empfängt, wenn das Durchgestrichene der Schriftart festgelegt ist, **andernfalls False.**

</dd> </dl>

Der Schriftschnitt, der in einem Sprechblasenzeichen für Zeichen verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Allerdings kann der Benutzer die Schriftarteinstellungen für alle Zeichen über das Eigenschaftenblatt des Microsoft-Agents überschreiben.

 

 




