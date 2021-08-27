---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb40b0be58695e79a02ab0ad67ad0d26a47bd13a1637dc1d1f5a4380a7429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749886"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Ruft die [**Beschriftung für**](caption-property.md) eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Die Adresse eines BSTR, der den Wert der Texteinstellung [**Caption**](caption-property.md) empfängt, die für eine [**Commands-Auflistung angezeigt**](/windows/desktop/lwef/the-commands-collection-object) wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)


 

 