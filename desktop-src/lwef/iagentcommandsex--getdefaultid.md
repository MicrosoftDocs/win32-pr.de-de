---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105226"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Ruft die ID des Standardbefehls in einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Adresse einer Variablen, die die ID des [**Befehlssatzes**](/windows/desktop/lwef/the-command-object) als Standard empfängt.

</dd> </dl>

Diese Eigenschaft gibt das aktuelle [**Command-Standardobjekt**](/windows/desktop/lwef/the-command-object) in Ihrer [**Commands-Auflistung zurück.**](/windows/desktop/lwef/the-commands-collection-object) Der Standardbefehl ist im Popupmenü des Zeichens fett formatiert. Das Festlegen des Standardbefehls ändert jedoch keine Befehlsbehandlung oder Doppelklickereignisse.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 