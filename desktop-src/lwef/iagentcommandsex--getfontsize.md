---
title: Iagentcommandsex GetFontSize
description: Iagentcommandsex GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388414"
---
# <a name="iagentcommandsexgetfontsize"></a>Iagentcommandsex:: GetFontSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Ruft den Wert für die Größe der Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plfontsize*
</dt> <dd>

Die Adresse eines Werts, der die Größe der Schriftart erhält.

</dd> </dl>

Die Punktgröße der zurückgegebenen Schriftart entspricht der Größe, die für die Anzeige von Text im Popup Menü des Zeichens definiert ist, wenn der Client für die Eingabe aktiviert ist. Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Menü Schriftart für die Sprach-ID-Einstellung des Zeichens oder, wenn nicht festgelegt, der Standard Spracheinstellung des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md), [ **iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md)


 

 




