---
title: Bereitstellen von Klassen Informationen
description: Bereitstellen von Klassen Informationen
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100699"
---
# <a name="providing-class-information"></a><span data-ttu-id="d8663-103">Bereitstellen von Klassen Informationen</span><span class="sxs-lookup"><span data-stu-id="d8663-103">Providing Class Information</span></span>

<span data-ttu-id="d8663-104">Es ist häufig sinnvoll, dass ein Client eines Objekts die Typinformationen des Objekts untersucht.</span><span class="sxs-lookup"><span data-stu-id="d8663-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="d8663-105">Aufgrund der CLSID des Objekts kann ein Client die Typbibliothek des Objekts mithilfe von Registrierungs Einträgen suchen und dann die Typbibliothek für den Co-Klassen Eintrag in der Bibliothek scannen, die der CLSID entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8663-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="d8663-106">Allerdings haben nicht alle Objekte eine CLSID, obwohl Sie weiterhin Typinformationen bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="d8663-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="d8663-107">Außerdem ist es für einen Client praktisch, eine Möglichkeit zu haben, ein Objekt einfach auf seine Typinformationen zu Fragen, anstatt alle Elemente aus Registrierungs Einträgen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="d8663-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="d8663-108">Diese Funktion ist wichtig, wenn Sie mit ausgehenden Schnittstellen auf Verbindungs fähigen Objekten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d8663-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="d8663-109">(Weitere Informationen zur Bereitstellung dieser Funktion durch Verbindungs fähige Objekte finden [Sie unter Verwenden von IProvideClassInfo](using-iprovideclassinfo.md) .)</span><span class="sxs-lookup"><span data-stu-id="d8663-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="d8663-110">In diesen Fällen kann ein Client das Objekt für [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)Abfragen.</span><span class="sxs-lookup"><span data-stu-id="d8663-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="d8663-111">Wenn diese Schnittstellen vorhanden sind, ruft der Client die [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) -Methode auf, um die Typinformationen für die Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8663-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="d8663-112">Durch die Implementierung von [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) oder [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)gibt ein Objekt an, dass es Typinformationen für die gesamte Klasse bereitstellen kann. Das heißt, was Sie in Ihrem Co-Klasse-Abschnitt Ihrer Typbibliothek beschreiben würde, wenn Sie eine hat.</span><span class="sxs-lookup"><span data-stu-id="d8663-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="d8663-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) gibt einen **ITypeInfo** -Zeiger zurück, der den Co-Klasse-Informationen des Objekts entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8663-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="d8663-114">Mithilfe dieses **ITypeInfo** -Zeigers kann der Client alle eingehenden und ausgehenden Schnittstellendefinitionen des Objekts überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d8663-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="d8663-115">Das-Objekt kann auch [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8663-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="d8663-116">Die **IProvideClassInfo2** -Schnittstelle ist eine einfache Erweiterung von [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) , mit der die ausgehenden Schnittstellen Bezeichner eines Objekts für den Standard Ereignis Satz schnell und einfach abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d8663-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="d8663-117">**IProvideClassInfo2** wird von **IProvideClassInfo** abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d8663-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8663-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8663-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8663-119">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="d8663-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




