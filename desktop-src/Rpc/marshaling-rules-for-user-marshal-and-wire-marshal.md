---
title: Marshallingregeln für user_marshal und wire_marshal
description: Die OSF-DCE-Spezifikation zum Marshallen eingebetteter Zeigertypen erfordert, dass Sie die folgenden Einschränkungen beachten, wenn Sie die Funktionen \_ UserSize, \_ UserMarshal und \_ UserUnMarshal implementieren.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883832"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Marshallingregeln für das \_ Marshallen von Benutzer und das Marshallen von \_ Wire

Die OSF-DCE-Spezifikation zum Marshallen eingebetteter Zeigertypen erfordert, dass Sie die folgenden Einschränkungen beachten, wenn Sie die Funktionen &lt; &gt; \_ UserSize, &lt; &gt; \_ UserMarshal und &lt; &gt; \_ UserUnMarshal implementieren. (Die hier angegebenen Regeln und Beispiele gelten für das Marshalling. Ihre Größen- und Unmarshalingroutinen müssen jedoch die gleichen Einschränkungen befolgen:

-   Wenn der Wire-Type ein flacher Typ ohne Zeiger ist, sollte Ihre Marshallingroutine für den entsprechenden userm-type die Daten einfach gemäß dem Layout des Wire-Typs marshallen. Beispiel:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Beachten Sie, dass der Kabeltyp **long** ein flacher Typ ist. Ihre HANDLE \_ HANDLE \_ UserMarshal-Funktion  marshallt lange, wenn ein HANDLE \_ HANDLE-Objekt an sie übergeben wird.

-   Wenn der wire-type ein Zeiger auf einen anderen Typ ist, sollte Ihre Marshallingroutine für den entsprechenden userm-type die Daten entsprechend dem Layout für den Typ marshallen, auf den der Wire-Typ zeigt. Die NDR-Engine übernimmt den Zeiger. Beispiel:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Beachten Sie, dass der Kabeltyp **WIRE \_ TYPE** ein Zeigertyp ist. Ihre HANDLE \_ DATA UserMarshal-Funktion marshallt die daten, die mit dem Handle verknüpft sind, mithilfe des HDATA-Layouts und nicht des \_ HDATA-Layouts. \*

-   Ein Wire-Typ muss entweder ein flacher Datentyp oder ein Zeigertyp sein. Wenn ihr transmissibler Typ etwas anderes sein muss (z. B. eine Struktur mit Zeigern), verwenden Sie einen Zeiger auf den gewünschten Typ als Wire-Type.

Diese Einschränkungen führen dazu, dass die typen, die mit den \[ [**Wire \_ Marshal-**](/windows/desktop/Midl/wire-marshal) oder \] \[ [**\_ Benutzer-Marshallattributen**](/windows/desktop/Midl/user-marshal) definiert wurden, \] frei in andere Typen eingebettet werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**\_Benutzer-Marshalling**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Der Typ \_ UserSize-Funktion](the-type-usersize-function.md)
</dt> <dt>

[Der Typ \_ UserMarshal-Funktion](the-type-usermarshal-function.md)
</dt> <dt>

[Thetype \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[Thetype \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 
