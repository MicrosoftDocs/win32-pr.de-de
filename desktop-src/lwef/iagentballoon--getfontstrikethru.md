---
title: Iagentballoon getfontstrikethru
description: Iagentballoon getfontstrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388717"
---
# <a name="iagentballoongetfontstrikethru"></a>Iagentballoon:: getfontstrikethru

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Gibt an, ob für die in einer Wort Sprechblase verwendete Schriftart der Stil des durch Streich Strichs festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbfontstrikethru*
</dt> <dd>

Die Adresse eines Werts, der **true** empfängt, wenn der Stil der Schriftart durchgestrichen festgelegt ist, andernfalls **false** .

</dd> </dl>

Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.

 

 




