---
title: Schalter "/robust"
description: Der Schalter /robust weist den MIDL-Compiler an, zusätzliche Fehlerüberprüfungsinformationen zu generieren, die die NDR-Engine verwendet, um Integritätsprüfungen zur Laufzeit durchzuführen.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robuster Switch MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551f5a60013aa3a903dcb3e35cc4c25a9f83dc67fff2a6ab5c7bfd62a041feee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895820"
---
# <a name="robust-switch"></a>Schalter "/robust"

Der **Schalter /robust** weist den MIDL-Compiler an, zusätzliche Fehlerüberprüfungsinformationen zu generieren, die die NDR-Engine verwendet, um Integritätsprüfungen zur Laufzeit durchzuführen.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/Oif* 
</dt> <dd>

Diese Schalter sind in ihrer Funktionalität identisch. Sie geben die codelose Proxymethode für das Marshalling an und verwenden schnelle Formatzeichenfolgen, um die Leistung zu verbessern. Siehe / [**Oi**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung des Schalters **/robust** generiert zusätzliche Informationen, die es der NDR-Engine (Network Data Representation, Netzwerkdatendarstellung) ermöglichen, Laufzeitfehlerüberprüfungen für korrelierte Argumente in dynamischen Arrays, Unions und in Out-Schnittstellenzeige in DCOM-Anwendungen durchzuführen. [](out-idl.md) Der **Schalter /robust** ist nur unter Windows 2000 und neueren Versionen von Windows.

Ein korreliertes Argument ist ein Argument, das eines der Attribute verwendet, mit denen die Größe eines Datenobjekts zur Laufzeit bestimmt werden kann: [**size \_ ist**](size-is.md), [**length \_ ist**](length-is.md), [**first \_ is**](first-is.md), [**last \_ is**](last-is.md), [**max \_ is**](max-is.md), [**switch \_ is**](switch-is.md), [**and iid \_ is**](iid-is.md). In Übereinstimmung mit der OSF-DCE-Spezifikation für die Wire-Darstellung wird dieses korrelierte Argument an zwei verschiedenen Stellen angezeigt. Stellen Sie sich beispielsweise vor, dass eine typische Verwendung des **-Attributs \_ "size"** ist:

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

In diesem Beispiel übergibt der Client einen long-Wert, der die Größe eines Blocks von BAR-TYPEs (in Bezug auf die Anzahl der BAR TYPES-Elemente) angibt, und einen Zeiger auf den tatsächlichen Block von \_ \_ \_ BAR-TYPEs. Das Size-Argument korreliert mit dem pBarType-Argument. In Übereinstimmung mit der OSF-DCE-Spezifikation wird das Size-Argument zweimal im Netzwerk dargestellt– zuerst als sich selbst und dann mit dem Array von BAR TYPE-Elementen, die das \_ pBarType-Argument darstellen. Jedes Argument wird unabhängig voneinander gemäß seiner eigenen Wire-Darstellung entmarshaliert. Normalerweise haben das Size-Argument und seine Kopie, die zur Darstellung eines Teils des anderen Arguments verwendet wird, dieselben Werte. Wenn das Size-Argument beschädigt wird (z. B. wenn der Block von BAR TYPES größer als der zugeordnete ist), reagiert die Serveranwendung möglicherweise nicht mehr, da sie den Wert des Arguments Size verwendet, um eingehende Daten zu \_ messen.

Der **Schalter /robust** ist erforderlich, um eine gültige Bereichsüberprüfung mit dem [**Bereichsattribut zu**](range.md) implementieren.

## <a name="examples"></a>Beispiele

**midl /robust /Oicf filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Bereich**](range.md)
</dt> </dl>

 

 




