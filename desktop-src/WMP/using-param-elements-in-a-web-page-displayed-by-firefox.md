---
title: Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird
description: Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows-Media Player, param-Elemente im Object-Element
- Windows Media Player-Objektmodell, param-Elemente im Object-Element
- Objektmodell, param-Elemente im Object-Element
- Windows Media Player Mobile, param-Elemente im Object-Element
- Windows Media Player ActiveX-Steuerelement, param-Elemente im Object-Element
- Windows Media Player Mobile ActiveX-Steuerelement, param-Elemente im Object-Element
- ActiveX-Steuerelement, param-Elemente im Object-Element
- Einbettungen, Webseiten
- Seiten Einbettung, param-Elemente im Object-Element
- Param-Elemente im Object-Element
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, param-Elemente im Object-Element
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311681"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Verwenden von param-Elementen in einer Webseite, die von Firefox angezeigt wird

Sie können param-Elemente innerhalb eines Object-Elements verwenden, um den Anfangszustand des Player-Steuer Elements festzulegen. Beispielsweise geben die param-Elemente im folgenden Beispiel an, dass das-Steuerelement automatisch Seattle. wmv abspielen soll.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



Die meisten param-Elemente können von Internet Explorer und Firefox interpretiert werden. Es gibt jedoch einige param-Elemente, die vom Firefox-Plug-in nicht unterstützt werden. Informationen darüber, welche param-Elemente vom Firefox-Plug-in unterstützt werden, finden Sie unter [param-Elemente in einem Object-Element](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




