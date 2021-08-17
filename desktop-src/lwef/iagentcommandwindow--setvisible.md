---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692643"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow::SetVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Legen Sie die [**Visible-Eigenschaft**](visible-property.md) für das Sprachbefehlsfenster fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

[**Sichtbare**](visible-property.md) Eigenschafteneinstellung. Der Wert **True** zeigt das Sprachbefehlsfenster an. **False** blendet sie aus.

</dd> </dl>

Der Benutzer kann diese Eigenschaft überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandWindow::GetVisible**](iagentcommandwindow--getvisible.md)


 

 




