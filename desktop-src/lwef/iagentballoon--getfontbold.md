---
title: Iagentballoon getfontbold
description: Iagentballoon getfontbold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206931"
---
# <a name="iagentballoongetfontbold"></a>Iagentballoon:: getfontbold

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart fett formatiert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbfontbold*
</dt> <dd>

Die Adresse eines Werts, der **true** erhält, wenn die Schriftart fett formatiert ist, und **false** , wenn Sie ungültig ist.

</dd> </dl>

Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.

 

 




