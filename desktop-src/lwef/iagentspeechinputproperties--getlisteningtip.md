---
title: Iagentspeechinputproperties getlisteningtip
description: Iagentspeechinputproperties getlisteningtip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339176"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>Iagentspeechinputproperties:: getlisteningtip

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Ruft einen Wert ab, der angibt, ob der Abhör Tipp für die Anzeige aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pblisteningtip*
</dt> <dd>

Die Adresse einer Variablen, die **true** empfängt, wenn der lausch Tipp für die Anzeige aktiviert ist, oder **false** , wenn der lauschyme deaktiviert ist.

</dd> </dl>

Wenn [**GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt, gibt die Abfrage von anderen Spracheingabe Eigenschaften einen Fehler zurück.

## <a name="see-also"></a>Weitere Informationen

[**Iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




