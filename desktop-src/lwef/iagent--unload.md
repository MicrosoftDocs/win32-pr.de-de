---
title: IAgent UnLoad
description: IAgent UnLoad
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610140"
---
# <a name="iagentunload"></a>IAgent::UnLoad

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Characters-Auflistung.**](/windows/desktop/lwef/the-characters-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Die ID des Zeichens.

</dd> </dl>

Verwenden Sie diese Methode, wenn Sie kein Zeichen mehr benötigen, um Arbeitsspeicher freizugeben, der zum Speichern von Informationen über das Zeichen verwendet wird. Wenn Sie erneut auf das Zeichen zugreifen, verwenden Sie die [**Load-Methode.**](load-method.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgent::Load**](iagent--load.md)


 

 