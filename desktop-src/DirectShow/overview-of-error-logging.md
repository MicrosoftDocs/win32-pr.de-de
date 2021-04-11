---
description: Übersicht über die Fehler Protokollierung
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Übersicht über die Fehler Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124369"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="b82e7-103">Übersicht über die Fehler Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b82e7-103">Overview of Error Logging</span></span>

<span data-ttu-id="b82e7-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="b82e7-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b82e7-105">Um Anwendungen maximale Flexibilität bei der Behandlung von Fehlern zu ermöglichen, verwenden [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) einen Rückrufmechanismus.</span><span class="sxs-lookup"><span data-stu-id="b82e7-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="b82e7-106">Die Anwendung implementiert eine Methode zum Protokollieren eines Fehlers.</span><span class="sxs-lookup"><span data-stu-id="b82e7-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="b82e7-107">Wenn zur Laufzeit ein Fehler auftritt, ruft der die von Ihnen bereitgestellte Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b82e7-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="b82e7-108">Die-Methode übernimmt Parameter, die den Fehler beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b82e7-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="b82e7-109">Die Methode, mit der diese Informationen verwendet werden, ist Ihnen überstehen.</span><span class="sxs-lookup"><span data-stu-id="b82e7-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="b82e7-110">(Es sollte jedoch so schnell wie möglich zurückgeben, oder es kann die Ausführung des Programms beeinträchtigen.)</span><span class="sxs-lookup"><span data-stu-id="b82e7-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="b82e7-111">Die Rückruf Methode für die Fehler Protokollierung ist in einer COM-Schnittstelle ( [**iamerrorlog**](iamerrorlog.md)) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b82e7-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="b82e7-112">Die Anwendung muss diese Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="b82e7-112">Your application must implement this interface.</span></span> <span data-ttu-id="b82e7-113">Wie alle COM-Schnittstellen erbt **iamerrorlog** die **IUnknown** -Schnittstelle, sodass die Anwendung dies ebenfalls implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="b82e7-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="b82e7-114">Sie haben mehrere Möglichkeiten, diese COM-Schnittstellen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="b82e7-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="b82e7-115">Sie können den Active Template Library (ATL) verwenden, der die vordefinierten Implementierungen der **IUnknown** -Methoden bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b82e7-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="b82e7-116">DirectShow bietet auch eine C++-Basisklasse ( [**cunknown**](cunknown.md)), mit der eine COM-Schnittstelle leicht implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b82e7-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="b82e7-117">Informationen zur Verwendung von **cunknown** finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b82e7-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="b82e7-118">Der Beispielcode in diesem Artikel definiert eine eigenständige C++-Klasse, die sowohl **IUnknown** als auch **iamerrorlog** implementiert.</span><span class="sxs-lookup"><span data-stu-id="b82e7-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="b82e7-119">Das Ergebnis ist kein echtes com-Objekt, da es **cokreateinstance** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b82e7-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="b82e7-120">Dieser Ansatz ist jedoch für den Zweck des Beispiels geeignet.</span><span class="sxs-lookup"><span data-stu-id="b82e7-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b82e7-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b82e7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b82e7-122">Protokollierungs Fehler</span><span class="sxs-lookup"><span data-stu-id="b82e7-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



