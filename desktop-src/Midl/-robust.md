---
title: /robust-Schalter
description: Der/robust-Schalter weist den Mittelwert Compiler an, zusätzliche Fehler Überprüfungs Informationen zu generieren, die von der NDR-Engine zur Ausführung von Integritätsprüfungen zur Laufzeit verwendet werden.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robust-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857239"
---
# <a name="robust-switch"></a>/robust-Schalter

Der **/robust** -Schalter weist den Mittelwert Compiler an, zusätzliche Fehler Überprüfungs Informationen zu generieren, die von der NDR-Engine zur Ausführung von Integritätsprüfungen zur Laufzeit verwendet werden.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/OIF* 
</dt> <dd>

Diese Switches sind in ihrer Funktionalität identisch. Sie geben die coschess-Proxy Methode für das Marshalling an und verwenden schnelle Format Zeichenfolgen, um die Leistung zu verbessern. Siehe/ [**Oi**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Durch die Verwendung des **/robust** -Schalters werden zusätzliche Informationen generiert, mit denen die Engine für die Netzwerkdaten Darstellung die Lauf Zeit Fehlerüberprüfung für korrelierte Argumente in dynamischen Arrays, Unions und in [**out**](out-idl.md) -Schnittstellen Zeigern in DCOM-Anwendungen ausführen kann. Der **/robust** -Schalter ist nur unter Windows 2000 und neueren Versionen von Windows verfügbar.

Bei einem korrelierten Argument handelt es sich um ein Argument, das eines der Attribute verwendet, mit denen die Größe eines Datenobjekts zur Laufzeit bestimmt werden kann: [**size \_ ist**](size-is.md), [**length \_ ist**](length-is.md), [**First \_ is**](first-is.md), [**Last \_ is**](last-is.md), [**Max \_ is**](max-is.md), [**Switch \_ is**](switch-is.md)und [**IID \_ ist**](iid-is.md). In Übereinstimmung mit der OSF-DCE-Spezifikation für die Wire-Darstellung wird dieses korrelierte Argument an zwei unterschiedlichen Stellen angezeigt. Nehmen wir beispielsweise an, eine typische Verwendung der **Größe \_ ist** "Attribute":

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

In diesem Beispiel übergibt der Client einen Long-Wert, der die Größe eines Blocks von Balken \_ Typen (in Bezug auf die Anzahl der Balken \_ Typen Elemente) und einen Zeiger auf den eigentlichen Block von Balken \_ Typen angibt. Das Größen Argument korreliert mit dem pbartype-Argument. In Übereinstimmung mit der OSF-DCE-Spezifikation wird das size-Argument zweimal im Netzwerk dargestellt – zuerst als sich selbst und dann mit dem Array von Bar- \_ Element-Elementen, die das pbartype-Argument darstellen. Jedes Argument wird gemäß seiner eigenen Wire-Darstellung unabhängig voneinander gemarshallt. Normalerweise haben das Größen Argument und seine Kopie, das zum Darstellen eines Teils des anderen Arguments verwendet wird, dieselben Werte. Wenn das Größen Argument jedoch beschädigt wird (z. b. wenn der Block mit den Balken \_ Typen größer ist als der zugeordnete Wert), reagiert die Serveranwendung möglicherweise nicht mehr, da Sie den Wert des Size-Arguments verwendet, um eingehende Daten zu messen.

Der **/robust** -Schalter ist erforderlich, um eine gültige Bereichs Überprüfung mit dem [**Range**](range.md) -Attribut zu implementieren.

## <a name="examples"></a>Beispiele

**Mittel l/robust/Oicf filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Bereich**](range.md)
</dt> </dl>

 

 




