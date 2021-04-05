---
title: Iagentcommandwindow setVisible
description: Iagentcommandwindow setVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037158"
---
# <a name="iagentcommandwindowsetvisible"></a>Iagentcommandwindow:: setVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Legen Sie die [**Visible**](visible-property.md) -Eigenschaft für das Fenster "Sprachbefehle" fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

[**Sichtbare**](visible-property.md) Eigenschafts Einstellung. Der Wert **true** zeigt das Fenster Sprachbefehle an. **False** blendet es aus.

</dd> </dl>

Der Benutzer kann diese Eigenschaft überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandwindow:: getVisible**](iagentcommandwindow--getvisible.md)


 

 




