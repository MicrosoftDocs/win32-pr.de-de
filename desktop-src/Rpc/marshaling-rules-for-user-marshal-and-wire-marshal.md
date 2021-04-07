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
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="fe5b2-103">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="fe5b2-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="fe5b2-104">Die OSF-DCE-Spezifikation für das Mars Hallen eingebetteter Zeiger Typen erfordert, dass Sie die folgenden Einschränkungen beachten, wenn Sie die <type> \_ Funktionen "usersize", " <type> \_ usermarshal" und " <type> \_ userunmarshal" implementieren.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="fe5b2-105">(Die hier aufgeführten Regeln und Beispiele sind für das Marshalling vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="fe5b2-106">Allerdings müssen für ihre Größen-und Marshallingroutinen dieselben Einschränkungen beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="fe5b2-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="fe5b2-107">Wenn der Wire-Typ ein flacher Typ ohne Zeiger ist, sollte die marshallingroutine für den entsprechenden userm-Type die Daten einfach gemäß dem Layout des Wire-Typs Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="fe5b2-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fe5b2-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="fe5b2-109">Beachten Sie, dass der Wire Type, **Long**, ein flacher Typ ist.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="fe5b2-110">Die usermarshal-Funktion des Handle-Handles \_ \_ marshallt einen **Long** -Wert, wenn ein Handle-Handle \_ an ihn weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="fe5b2-111">Wenn der Wire-Type ein Zeiger auf einen anderen Typ ist, sollte die marshallingroutine für den entsprechenden userm-Type die Daten gemäß dem Layout für den Typ Mars Hallen, auf den der Wire-Typ verweist.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="fe5b2-112">Die NDR-Engine übernimmt den-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="fe5b2-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fe5b2-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="fe5b2-114">Beachten Sie, dass der Wire Type, **Wire \_ Type**, ein Zeigertyp ist.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="fe5b2-115">Ihre Handle \_ Data \_ usermarshal-Funktion marshallt die mit dem Handle verknüpften Daten, wobei das hdata-Layout anstelle des hdata-Layouts verwendet wird \* .</span><span class="sxs-lookup"><span data-stu-id="fe5b2-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="fe5b2-116">Ein Wire-Type muss entweder ein flacher Datentyp oder ein Zeigertyp sein.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="fe5b2-117">Wenn Ihr übertragbarer Typ etwas anderes sein muss (z. b. eine Struktur mit Zeigern), verwenden Sie einen Zeiger auf den gewünschten Typ als Wire-Type.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="fe5b2-118">Die Auswirkung dieser Einschränkungen besteht darin, dass die mit den Attributen " \[ [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) " oder " \] \[ [**User \_ Marshal**](/windows/desktop/Midl/user-marshal) " definierten Typen \] frei in andere Typen eingebettet werden können.</span><span class="sxs-lookup"><span data-stu-id="fe5b2-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe5b2-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe5b2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5b2-120">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="fe5b2-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="fe5b2-121">**Benutzer \_ Mars Hall**</span><span class="sxs-lookup"><span data-stu-id="fe5b2-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="fe5b2-122">Die Type \_ usersize-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe5b2-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="fe5b2-123">Der Typ \_ usermarshal-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe5b2-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="fe5b2-124">\_Userunmarshalfunction-Typ</span><span class="sxs-lookup"><span data-stu-id="fe5b2-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="fe5b2-125">\_Userfrefunction-Typ</span><span class="sxs-lookup"><span data-stu-id="fe5b2-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 