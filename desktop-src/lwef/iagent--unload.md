---
title: Iagent entladen
description: Iagent entladen
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315050"
---
# <a name="iagentunload"></a>Iagent:: entladen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Die ID des Zeichens.

</dd> </dl>

Verwenden Sie diese Methode, wenn Sie kein Zeichen mehr benötigen, um Arbeitsspeicher freizugeben, der zum Speichern von Informationen über das Zeichen verwendet wird. Wenn Sie erneut auf das Zeichen zugreifen, verwenden Sie die [**Load**](load-method.md) -Methode.

## <a name="see-also"></a>Weitere Informationen

[**Iagent:: Load**](iagent--load.md)


 

 