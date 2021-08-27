---
title: IAgent-Registrierung aufheben
description: IAgent-Registrierung aufheben
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976480"
---
# <a name="iagentunregister"></a>IAgent::Unregister

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Characters-Auflistung.**](/windows/desktop/lwef/the-characters-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

Die ID der Benachrichtigungssenke.

</dd> </dl>

Verwenden Sie diese Methode, wenn Sie microsoft-Agent-Dienste nicht mehr benötigen, z. B. wenn Ihre Anwendung heruntergefahren wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgent::Register**](iagent--register.md)


 

 