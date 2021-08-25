---
title: Mehrere Zeigerebenen
description: Verwenden mehrerer Zeigerebenen im Remoteprozeduraufruf (REMOTE Procedure Call, RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c4424679f69daf3a5d88f137d55bd485824ef08498266882d84931a6d03f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019640"
---
# <a name="multiple-levels-of-pointers"></a>Mehrere Zeigerebenen

Wenn es mehrere Ebenen von Zeigern gibt, werden die Attribute dem Zeiger zugeordnet, der dem Variablennamen am nächsten ist. Der Client ist weiterhin für die Zuweisung von Speicher verantwortlich, der der Antwort zugeordnet ist.

Im folgenden Beispiel kann der Stub den Server aufrufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden:

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

In diesem Beispiel übergibt der Stub dem Server einen eindeutigen Zeiger, den der Server mit **NULL initialisiert.** Der Server ordnet dann einen Block von BARs zu, legt den Zeiger fest, legt das Größenargument fest und gibt zurück. Beachten Sie, dass Sie einen Verweiszeiger an einen eindeutigen Zeiger auf Ihre Daten übergeben müssen, damit der Server auswirkungen auf \[ \] den \[ [](/windows/desktop/Midl/unique) \] Aufrufer hat. Beachten Sie auch, dass das Komma in der Größe ( \[ [**\_**](/windows/desktop/Midl/size-is), pSize ) ist, was angibt, dass der Zeiger der obersten Ebene kein Zeiger der Größe ist, sondern dass der Zeiger auf niedrigerer Ebene \* \] ist.

Auf Clientseite legt der Stub ppBar auf \* **NULL fest,** bevor die Remoteprozedur aufruft. Der Stub ordnet dann den Arry von BAR-Objekten zu und entmarshaliert diesen. Das size-Argument gibt die Größe des Blocks (und die Anzahl der nichtmarshalierten BARs) an. Der Client muss das zurückgegebene Array von BAR-Objekten frei geben, wenn es nicht mehr benötigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**size \_ ist**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 