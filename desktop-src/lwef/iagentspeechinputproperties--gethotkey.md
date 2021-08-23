---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609380"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Ruft die aktuelle Tastaturzuweisung für die Spracheingabe-Abhörtaste ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Adresse eines BSTR, der die aktuelle Hotkeyeinstellung empfängt, die zum Öffnen des Audiokanals für die Spracheingabe verwendet wird.

</dd> </dl>

Wenn [**GetEnabled False**](iagentspeechinputproperties--getenabled.md) **zurückgibt,** löst das Abfragen dieser Einstellung einen Fehler aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




