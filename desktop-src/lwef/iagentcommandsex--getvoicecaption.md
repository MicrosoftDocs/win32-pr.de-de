---
title: Iagentcommandsex getvoicecaption
description: Iagentcommandsex getvoicecaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337646"
---
# <a name="iagentcommandsexgetvoicecaption"></a>Iagentcommandsex:: getvoicecaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Ruft die [**voicecaption**](voicecaption-property.md) für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszvoicecaption*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert des [**Beschriftungs**](caption-property.md) Texts empfängt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> </dl>

Der zurückgegebene Text ist, der für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt festgelegt wird und im Fenster "Sprachbefehle" angezeigt wird, wenn die Client Anwendung aktiv ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: setvoicecaption**](iagentcommandsex--setvoicecaption.md)


 

 