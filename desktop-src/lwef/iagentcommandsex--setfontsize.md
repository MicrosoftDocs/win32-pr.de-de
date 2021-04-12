---
title: Iagentcommandsex SetFontSize
description: Iagentcommandsex SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472860"
---
# <a name="iagentcommandsexsetfontsize"></a>Iagentcommandsex:: SetFontSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Legt die Größe der Schriftart fest, die im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lfontsize*
</dt> <dd>

Der Schriftgrad.

</dd> </dl>

Diese Eigenschaft bestimmt die Punktgröße der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird, wenn die Client Anwendung aktiv ist. Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Einstellung des Menüs für die Sprach-ID-Einstellung des Zeichens oder, wenn dies nicht festgelegt ist, der Standard Spracheinstellung des Benutzers. Wenn die Eingabe nicht aktiv ist, wird der Text der [**Befehls**](/windows/desktop/lwef/the-command-object) [**Beschriftung**](caption-property.md) der Client Anwendung in der für den Eingabe aktiven Client angegebenen Punktgröße angezeigt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: GetFontSize**](iagentcommandsex--getfontsize.md), [**iagentcommandsex:: getfontname**](iagentcommandsex--getfontname.md), [**iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md)


 

 