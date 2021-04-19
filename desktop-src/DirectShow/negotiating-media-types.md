---
description: Aushandeln von Medientypen
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Aushandeln von Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361771"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="f4b78-103">Aushandeln von Medientypen</span><span class="sxs-lookup"><span data-stu-id="f4b78-103">Negotiating Media Types</span></span>

<span data-ttu-id="f4b78-104">Wenn der Filter Graph-Manager die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode aufruft, verfügt er über mehrere Optionen zum Angeben eines Medientyps:</span><span class="sxs-lookup"><span data-stu-id="f4b78-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="f4b78-105">**Complete Type:** Wenn der Medientyp vollständig angegeben ist, versuchen die Pins, eine Verbindung mit diesem Typ herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f4b78-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="f4b78-106">Wenn dies nicht möglich ist, schlägt der Verbindungsversuch fehl.</span><span class="sxs-lookup"><span data-stu-id="f4b78-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="f4b78-107">**Partieller Medientyp:** Ein Medientyp ist *partiell* , wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f4b78-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="f4b78-108">Der Wert GUID \_ Null fungiert als "Platzhalter", der angibt, dass ein beliebiger Wert zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f4b78-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="f4b78-109">Die Pins verhandeln einen Typ, der mit dem partiellen Typ konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="f4b78-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="f4b78-110">**Kein Medientyp:** Wenn der Filter Diagramm-Manager einen **null** -Zeiger übergibt, können die Pins allen Medientypen zustimmen, die für beide Pins zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f4b78-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="f4b78-111">Wenn die Pins eine Verbindung herstellen, verfügt die Verbindung immer über einen kompletten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="f4b78-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="f4b78-112">Der Medientyp, der vom Filter Graph-Manager angegeben wird, besteht darin, die möglichen Verbindungstypen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="f4b78-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="f4b78-113">Während des Aushandlungs Prozesses schlägt die Ausgabe-PIN einen Medientyp vor, indem die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode der Eingabe-PIN aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f4b78-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="f4b78-114">Die Eingabe-PIN kann den vorgeschlagenen Typ akzeptieren oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="f4b78-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="f4b78-115">Dieser Prozess wird wiederholt, bis entweder die Eingabe-PIN einen Typ annimmt, oder wenn die Ausgabe-PIN nicht mehr von den Typen ausgeht und die Verbindung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f4b78-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="f4b78-116">Gibt an, wie eine Ausgabe-PIN die anzuzeigende Medientypen auswählt.</span><span class="sxs-lookup"><span data-stu-id="f4b78-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="f4b78-117">In den DirectShow-Basisklassen Ruft die Ausgabepin [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) auf der Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="f4b78-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="f4b78-118">Diese Methode gibt einen Enumerator zurück, der die bevorzugten Medientypen der Eingabe-PIN auflistet.</span><span class="sxs-lookup"><span data-stu-id="f4b78-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="f4b78-119">Wenn ein Fehler auftritt, listet die Ausgabe-PIN die eigenen bevorzugten Typen auf.</span><span class="sxs-lookup"><span data-stu-id="f4b78-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="f4b78-120">**Arbeiten mit Medientypen**</span><span class="sxs-lookup"><span data-stu-id="f4b78-120">**Working with Media Types**</span></span>

<span data-ttu-id="f4b78-121">Überprüfen Sie in jeder Funktion, die einen **am- \_ \_ Medientyp** -Parameter empfängt, immer die Werte von **cbformat** und **Format Type** , bevor Sie den **pbformat** -Member dereferenzieren.</span><span class="sxs-lookup"><span data-stu-id="f4b78-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="f4b78-122">Der folgende Code ist falsch:</span><span class="sxs-lookup"><span data-stu-id="f4b78-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="f4b78-123">Der folgende Code ist korrekt:</span><span class="sxs-lookup"><span data-stu-id="f4b78-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



