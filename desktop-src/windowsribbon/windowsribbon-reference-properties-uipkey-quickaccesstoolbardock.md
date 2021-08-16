---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifiziert die \_ PKEY \_ QuickAccessToolbarDock-Eigenschaft der Benutzeroberfläche.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9011cceb9b2ec96680ea3badd0ad40ae6121c14a70e065cfbfff5f5fe8e1f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201378"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

Identifiziert die \_ PKEY \_ QuickAccessToolbarDock-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Hinweise

Ui PKEY QuickAccessToolbarDock wird von einer Anwendung verwendet, um den Andockzustand der Symbolleiste für den Schnellzugriff \_ \_ (QAT) abfragt.

Der Eigenschaftswert ist aus der [**\_ CONTROLDOCK-Enumeration der UI.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock)



|    Enumeration                     |    Beschreibung                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_UI-STEUERELEMENTDOCK \_ TOP    | Die QAT wird im Nicht-Clientbereich der Menübandhostanwendung angedockt, wie im folgenden Screenshot gezeigt.![Screenshot der Symbolleiste für den Schnellzugriff, die über dem Menüband im Nicht-Clientbereich angedockt ist.](images/properties/qat-docktop.png)<br/> |
| UI \_ CONTROLDOCK \_ BOTTOM | Die QAT wird wie im folgenden Screenshot gezeigt als visuell integrales Band unterhalb des Menübands angedockt. ![Screenshot der Symbolleiste für den Schnellzugriff, die unter dem Menüband angedockt ist.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Menübandeigenschaften](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

