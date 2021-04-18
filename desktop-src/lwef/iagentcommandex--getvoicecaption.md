---
title: Iagentcommandex getvoicecaption
description: Iagentcommandex getvoicecaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f367a7956d1029eae47064a0778264e3b77f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314732"
---
# <a name="iagentcommandexgetvoicecaption"></a>Iagentcommandex:: getvoicecaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Ruft die [**voicecaption**](voicecaption-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszvoicecaption*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert des [**Beschriftungs**](caption-property.md) Texts empfängt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> </dl>

Die [**voicecaption**](voicecaption-property.md) ist der Text, der für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt im Fenster "Sprachbefehle" angezeigt wird, wenn die Client Anwendung aktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandex:: setvoicecaption**](iagentcommandex--setvoicecaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommandsex:: Addex**](iagentcommandsex--addex.md), [**iagentcommandsex:: insertex**](iagentcommandsex--insertex.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 