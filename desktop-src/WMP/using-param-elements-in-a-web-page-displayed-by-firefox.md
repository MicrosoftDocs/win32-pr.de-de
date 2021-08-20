---
title: Verwenden von PARAM-Elementen auf einer webseite, die von Firefox angezeigt wird
description: Verwenden von PARAM-Elementen auf einer webseite, die von Firefox angezeigt wird
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player,PARAM-Elemente im OBJECT-Element
- Windows Media Player Objektmodell, PARAM-Elemente im OBJECT-Element
- Objektmodell, PARAM-Elemente im OBJECT-Element
- Windows Media Player Mobile,PARAM-Elemente im OBJECT-Element
- Windows Media Player ActiveX,PARAM-Elemente im OBJECT-Element
- Windows Media Player Mobile ActiveX-Steuerelement, PARAM-Elemente im OBJECT-Element
- ActiveX,PARAM-Elemente im OBJECT-Element
- Einbetten, Webseiten
- Einbetten von Webseiten, PARAM-Elemente in OBJECT-Element
- PARAM-Elemente im OBJECT-Element
- Windows Media Player,Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobil, Firefox
- Windows Media Player ActiveX,Firefox
- Windows Media Player Mobile ActiveX-Steuerelement,Firefox
- ActiveX,Firefox
- Firefox,PARAM-Elemente im OBJECT-Element
- Einbetten von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767b9b0d5e4367a17f07f68600ff8e9cac488ca9e4c950165d84677fd7d03956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117305"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Verwenden von PARAM-Elementen auf einer webseite, die von Firefox angezeigt wird

Sie können PARAM-Elemente in einem OBJECT-Element verwenden, um den Anfangszustand des Player-Steuerelements zu festlegen. Beispielsweise geben die PARAM-Elemente im folgenden Beispiel an, dass das Steuerelement "seattle.wmv" automatisch wieder geben soll.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



Die meisten PARAM-Elemente können von Internet Explorer firefox interpretiert werden. Es gibt jedoch einige PARAM-Elemente, die das Firefox-Plug-In nicht unterstützt. Informationen dazu, welche PARAM-Elemente vom Firefox-Plug-In unterstützt werden, finden Sie unter [PARAM-Elemente in einem OBJECT-Element.](param-elements-in-an-object-element.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuerelements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




