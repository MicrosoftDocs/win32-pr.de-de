---
title: Iagentcommandex setvoicecaption
description: Iagentcommandex setvoicecaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038824"
---
# <a name="iagentcommandexsetvoicecaption"></a>Iagentcommandex:: setvoicecaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Legt den für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigten [**voicecaption**](voicecaption-property.md) -Text fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*
</dt> <dd>

Ein BSTR, der den Text für die [**voicecaption**](voicecaption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest. Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text. Wenn weder die **voicecaption** -Eigenschaft noch die-Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

[**Caption**](caption-property.md)

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommandsex:: Addex**](iagentcommandsex--addex.md), [**iagentcommandsex:: insertex**](iagentcommandsex--insertex.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 