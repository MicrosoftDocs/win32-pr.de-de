---
title: Iagentcommandsex setvoicecaption
description: Iagentcommandsex setvoicecaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339269"
---
# <a name="iagentcommandsexsetvoicecaption"></a>Iagentcommandsex:: setvoicecaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Legt den für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt angezeigten [**voicecaption**](voicecaption-property.md) -Text fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszvoicecaption*
</dt> <dd>

Ein BSTR, der den Text für die [**voicecaption**](voicecaption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest. Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text. Wenn weder die **voicecaption** -Eigenschaft noch die **Caption** -Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: getvoicecaption**](iagentcommandsex--getvoicecaption.md)


 

 