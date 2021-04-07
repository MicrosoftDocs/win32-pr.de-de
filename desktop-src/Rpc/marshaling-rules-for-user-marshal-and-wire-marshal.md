---
title: Marshalling von Regeln für user_marshal und Wire_marshal
description: Die OSF-DCE-Spezifikation für das Mars Hallen eingebetteter Zeiger Typen erfordert, dass Sie die folgenden Einschränkungen beachten, wenn Sie den Typ \_ usersize, Type \_ usermarshal und Type \_ userunmarshal-Funktionen implementieren.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728857"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_

Die OSF-DCE-Spezifikation für das Mars Hallen eingebetteter Zeiger Typen erfordert, dass Sie die folgenden Einschränkungen beachten, wenn Sie die <type> \_ Funktionen "usersize", " <type> \_ usermarshal" und " <type> \_ userunmarshal" implementieren. (Die hier aufgeführten Regeln und Beispiele sind für das Marshalling vorgesehen. Allerdings müssen für ihre Größen-und Marshallingroutinen dieselben Einschränkungen beachtet werden:

-   Wenn der Wire-Typ ein flacher Typ ohne Zeiger ist, sollte die marshallingroutine für den entsprechenden userm-Type die Daten einfach gemäß dem Layout des Wire-Typs Mars Hallen. Beispiel:

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    Beachten Sie, dass der Wire Type, **Long**, ein flacher Typ ist. Die usermarshal-Funktion des Handle-Handles \_ \_ marshallt einen **Long** -Wert, wenn ein Handle-Handle \_ an ihn weitergeleitet wird.

-   Wenn der Wire-Type ein Zeiger auf einen anderen Typ ist, sollte die marshallingroutine für den entsprechenden userm-Type die Daten gemäß dem Layout für den Typ Mars Hallen, auf den der Wire-Typ verweist. Die NDR-Engine übernimmt den-Zeiger. Beispiel:

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    Beachten Sie, dass der Wire Type, **Wire \_ Type**, ein Zeigertyp ist. Ihre Handle \_ Data \_ usermarshal-Funktion marshallt die mit dem Handle verknüpften Daten, wobei das hdata-Layout anstelle des hdata-Layouts verwendet wird \* .

-   Ein Wire-Type muss entweder ein flacher Datentyp oder ein Zeigertyp sein. Wenn Ihr übertragbarer Typ etwas anderes sein muss (z. b. eine Struktur mit Zeigern), verwenden Sie einen Zeiger auf den gewünschten Typ als Wire-Type.

Die Auswirkung dieser Einschränkungen besteht darin, dass die mit den Attributen " \[ [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) " oder " \] \[ [**User \_ Marshal**](/windows/desktop/Midl/user-marshal) " definierten Typen \] frei in andere Typen eingebettet werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**Benutzer \_ Mars Hall**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Die Type \_ usersize-Funktion](the-type-usersize-function.md)
</dt> <dt>

[Der Typ \_ usermarshal-Funktion](the-type-usermarshal-function.md)
</dt> <dt>

[\_Userunmarshalfunction-Typ](the-type-userunmarshal-function.md)
</dt> <dt>

[\_Userfrefunction-Typ](the-type-userfree-function.md)
</dt> </dl>

 

 