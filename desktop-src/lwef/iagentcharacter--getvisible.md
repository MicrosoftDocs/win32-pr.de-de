---
title: Iagentcharacter getVisible
description: Iagentcharacter getVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101486"
---
# <a name="iagentcharactergetvisible"></a>Iagentcharacter:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Bestimmt, ob der Animations Rahmen des Zeichens momentan sichtbar ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn der Rahmen des Zeichens sichtbar ist, und **false** , wenn Sie ausgeblendet ist.

</dd> </dl>

Sie können diese Methode verwenden, um zu bestimmen, ob der Rahmen des Zeichens momentan sichtbar ist. Verwenden Sie die [**Show**](/windows/desktop/lwef/iagentcharacter--show) -Methode, um ein Zeichen sichtbar zu machen. Um ein Zeichen auszublenden, verwenden Sie die [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) -Methode.

 

 