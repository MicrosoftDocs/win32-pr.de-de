---
title: Iagentspeechinputproperties GetHotKey
description: Iagentspeechinputproperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036227"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>Iagentspeechinputproperties:: GetHotKey

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Ruft die aktuelle Tastatur Zuweisung für den Schlüssel für die Spracheingabe Überwachung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszhotcharkey*
</dt> <dd>

Adresse eines BSTR, das die aktuelle Hotkey-Einstellung empfängt, mit der der Audiokanal für die Spracheingabe geöffnet wird.

</dd> </dl>

Wenn [**GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt, löst eine Abfrage dieser Einstellung einen Fehler aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




