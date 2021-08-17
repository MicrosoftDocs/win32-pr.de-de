---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b348904020a53eb11d2bb7884a05f8d98e223a359f796e7d891dafb3dcc402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105335"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands::GetVoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Ruft den Wert der [**Voice-Eigenschaft**](voice-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Die Adresse eines BSTR, der den Wert der [**Sprachtexteinstellung**](voice-property.md) für eine [**Commands-Sammlung empfängt.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::SetVoice,**](iagentcommands--setvoice.md) [**IAgentCommands::GetCaption,**](iagentcommands--getcaption.md) [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)


 

 