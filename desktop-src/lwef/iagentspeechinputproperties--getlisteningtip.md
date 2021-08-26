---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0199e75ad56cee2c299ce53be3aa94376104af5ead40004e8dbbd8fd4dcfec9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014180"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Ruft einen Wert ab, der angibt, ob der Lauschende Tipp für die Anzeige aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Adresse einer Variablen, die **True** empfängt, wenn der Lauschende Tipp für die Anzeige aktiviert ist, oder **False,** wenn der Lauschende Tipp deaktiviert ist.

</dd> </dl>

Wenn [**GetEnabled**](iagentspeechinputproperties--getenabled.md) **False** zurückgibt, wird beim Abfragen anderer Spracheingabeeigenschaften ein Fehler zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




