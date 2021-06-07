---
title: Rückgabewerte (Windows-Barrierefreiheitsfeatures)
description: In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener zu sehen sind.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443991"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="8ef21-103">Rückgabewerte (Windows-Barrierefreiheitsfeatures)</span><span class="sxs-lookup"><span data-stu-id="8ef21-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="8ef21-104">In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener zu sehen sind.</span><span class="sxs-lookup"><span data-stu-id="8ef21-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="8ef21-105">Allgemeine Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ef21-105">Common Return Values</span></span>

<span data-ttu-id="8ef21-106">Die [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) geben einen der folgenden Werte zurück, der in winerror.h definiert ist, oder einen anderen standard Component Object Model (COM)-Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="8ef21-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="8ef21-107">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef21-107">Value</span></span>                      |   <span data-ttu-id="8ef21-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ef21-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef21-109">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="8ef21-109">S\_OK</span></span>                   | <span data-ttu-id="8ef21-110">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ef21-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8ef21-111">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="8ef21-111">S\_FALSE</span></span>                | <span data-ttu-id="8ef21-112">Die -Methode war teilweise erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8ef21-112">The method succeeded in part.</span></span> <span data-ttu-id="8ef21-113">Dies geschieht, wenn die Methode erfolgreich ist, die angeforderten Informationen jedoch nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8ef21-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="8ef21-114">Beispielsweise gibt Microsoft Active Accessibility S FALSE zurück, wenn Sie \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) aufrufen, um ein untergeordnetes Objekt an einem bestimmten Punkt abzurufen, und der angegebene Punkt nicht innerhalb des Objekts oder des untergeordneten Objekts liegt.</span><span class="sxs-lookup"><span data-stu-id="8ef21-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="8ef21-115">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8ef21-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="8ef21-116">Das -Objekt unterstützt die angeforderte Eigenschaft oder Aktion nicht.</span><span class="sxs-lookup"><span data-stu-id="8ef21-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="8ef21-117">Beispielsweise gibt eine Pushschaltfläche diesen Wert zurück, wenn Sie die [Value-Eigenschaft](value-property.md)anfordern, da sie keine Value-Eigenschaft hat.</span><span class="sxs-lookup"><span data-stu-id="8ef21-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8ef21-118">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8ef21-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="8ef21-119">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8ef21-119">The method is not implemented.</span></span> <span data-ttu-id="8ef21-120">Dieser Wert tritt auf, wenn ein Client eine Methode aufruft, die in diesem Betriebssystem noch nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8ef21-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8ef21-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8ef21-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="8ef21-122">Mindestens ein Argument war ungültig.</span><span class="sxs-lookup"><span data-stu-id="8ef21-122">One or more arguments were not valid.</span></span> <span data-ttu-id="8ef21-123">Dieser Fehler tritt auf, wenn der Aufrufer versucht, ein untergeordnetes Objekt mithilfe eines Bezeichners zu identifizieren, der vom Server nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="8ef21-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="8ef21-124">Dieser Fehler tritt auch auf, wenn ein Client versucht, ein untergeordnetes Objekt in einem Objekt zu identifizieren, das keine untergeordneten Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="8ef21-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="8ef21-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8ef21-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="8ef21-126">Die -Methode konnte keinen Arbeitsspeicher zuordnen, der zum Abschließen eines vorgangs erforderlich ist, der für den Erfolg entscheidend ist.</span><span class="sxs-lookup"><span data-stu-id="8ef21-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8ef21-127">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="8ef21-127">E\_FAIL</span></span>                 | <span data-ttu-id="8ef21-128">Unbekannter oder generischer Fehler.</span><span class="sxs-lookup"><span data-stu-id="8ef21-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="8ef21-129">Zusätzliche Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8ef21-129">Additional Return Values</span></span>

<span data-ttu-id="8ef21-130">Im Folgenden finden Sie Rückgabewerte, die [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="8ef21-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="8ef21-131">Diese Rückgabewerte sind nicht so häufig wie die vorherigen, aber Sie sollten sie kennen.</span><span class="sxs-lookup"><span data-stu-id="8ef21-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="8ef21-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef21-132">Value</span></span>                    |    <span data-ttu-id="8ef21-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ef21-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef21-134">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="8ef21-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="8ef21-135">Dies wird zurückgegeben, wenn Sie get \_ accValue aufrufen, um den Wert eines Kennwortsteuerworts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ef21-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="8ef21-136">DISP \_ E \_ EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="8ef21-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="8ef21-137">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="8ef21-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




