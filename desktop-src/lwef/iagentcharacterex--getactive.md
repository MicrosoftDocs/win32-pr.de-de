---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f9cb05143d4948fbcae1f8d9ed74a7216c5a2520b28f4c299321bcbac4272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478028"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Ruft ab, ob ihre Clientanwendung der aktive Client des Zeichens ist und ob das Zeichen am höchsten ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Adresse einer Variablen, die einen der folgenden Werte für die Statuseinstellung empfängt:



| Wert                                                              | BESCHREIBUNG                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Ihr Client ist nicht der aktive Client des Zeichens.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Ihr Client ist der aktive Client des Zeichens.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Ihr Client ist eingabeaktiv (aktiver Client des obersten Zeichens). |



 

</dd> </dl>

Mit dieser Einstellung erfahren Sie, ob Sie der aktive Client des Zeichens sind oder ob es sich bei Ihrem Zeichen um das aktive Eingabezeichen handelt. Wenn mehrere Clientanwendungen das gleiche Zeichen verwenden, empfängt der aktive Client des Zeichens Mauseingaben (z. B. Klick- oder Ziehereignisse des Microsoft-Agent-Steuerelements). Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als eingabeaktiver Client bezeichnet) [**IAgentNotifySink::Command-Ereignisse.**](iagentnotifysink--command.md)

Verwenden Sie die [**Activate-Methode,**](iagentcharacter--activate.md) um festzulegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder um Ihre Anwendung zum aktiven Eingabeclient zu machen (wodurch das Zeichen auch ganz oben steht).

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





