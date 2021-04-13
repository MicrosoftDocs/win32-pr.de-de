---
title: Rückgabewerte (Windows-Barrierefreiheits Funktionen)
description: In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener angezeigt werden.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474772"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="b239e-103">Rückgabewerte (Windows-Barrierefreiheits Funktionen)</span><span class="sxs-lookup"><span data-stu-id="b239e-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="b239e-104">In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b239e-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="b239e-105">Allgemeine Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b239e-105">Common Return Values</span></span>

<span data-ttu-id="b239e-106">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden geben einen der folgenden Werte zurück, die in WinError. h definiert sind, oder einen anderen Standard Component Object Model (com)-Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="b239e-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b239e-107">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="b239e-107">S\_OK</span></span>                   | <span data-ttu-id="b239e-108">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b239e-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b239e-109">S \_ false</span><span class="sxs-lookup"><span data-stu-id="b239e-109">S\_FALSE</span></span>                | <span data-ttu-id="b239e-110">Die Methode war teilweise erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b239e-110">The method succeeded in part.</span></span> <span data-ttu-id="b239e-111">Dies ist der Fall, wenn die Methode erfolgreich ist, die angeforderten Informationen aber nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b239e-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="b239e-112">Beispielsweise gibt Microsoft Active Accessibility S \_ false zurück, wenn Sie [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) aufrufen, um ein untergeordnetes Objekt an einem bestimmten Punkt abzurufen, und der angegebene Punkt nicht innerhalb des Objekts oder des untergeordneten Objekts liegt.</span><span class="sxs-lookup"><span data-stu-id="b239e-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="b239e-113">DISP \_ E \_ mitgliednotfound</span><span class="sxs-lookup"><span data-stu-id="b239e-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="b239e-114">Das Objekt unterstützt die angeforderte Eigenschaft oder Aktion nicht.</span><span class="sxs-lookup"><span data-stu-id="b239e-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="b239e-115">Beispielsweise gibt eine Push-Schaltfläche diesen Wert zurück, wenn Sie die [Value-Eigenschaft](value-property.md)anfordern, da Sie nicht über eine Value-Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="b239e-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="b239e-116">E \_ notimpl</span><span class="sxs-lookup"><span data-stu-id="b239e-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="b239e-117">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b239e-117">The method is not implemented.</span></span> <span data-ttu-id="b239e-118">Dieser Wert tritt auf, wenn ein Client eine Methode aufruft, die in diesem Betriebssystem noch nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b239e-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b239e-119">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="b239e-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="b239e-120">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b239e-120">One or more arguments were not valid.</span></span> <span data-ttu-id="b239e-121">Dieser Fehler tritt auf, wenn der Aufrufer versucht, ein untergeordnetes Objekt mithilfe eines Bezeichners zu identifizieren, der vom Server nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="b239e-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="b239e-122">Dieser Fehler tritt auch dann auf, wenn ein Client versucht, ein untergeordnetes Objekt innerhalb eines Objekts zu identifizieren, das keine untergeordneten Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="b239e-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="b239e-123">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="b239e-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="b239e-124">Die Methode konnte keinen Arbeitsspeicher zuweisen, der zum Durchführen eines Vorgangs erforderlich ist, der für den Erfolg entscheidend ist.</span><span class="sxs-lookup"><span data-stu-id="b239e-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b239e-125">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="b239e-125">E\_FAIL</span></span>                 | <span data-ttu-id="b239e-126">Ein unbekannter oder generischer Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b239e-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="b239e-127">Zusätzliche Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b239e-127">Additional Return Values</span></span>

<span data-ttu-id="b239e-128">Im folgenden finden Sie Rückgabewerte, die von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="b239e-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="b239e-129">Diese Rückgabewerte sind nicht so häufig wie die vorherigen Werte, Sie sollten sich jedoch bewusst sein.</span><span class="sxs-lookup"><span data-stu-id="b239e-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b239e-130">E \_ AccessDenied</span><span class="sxs-lookup"><span data-stu-id="b239e-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="b239e-131">Dies wird zurückgegeben, wenn Sie get \_ accValue zum Abrufen des Werts eines Kenn Wort Steuer Elements abrufen.</span><span class="sxs-lookup"><span data-stu-id="b239e-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="b239e-132">DISP \_ E- \_ Ausnahme</span><span class="sxs-lookup"><span data-stu-id="b239e-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="b239e-133">Co \_ E \_ objnotconnected</span><span class="sxs-lookup"><span data-stu-id="b239e-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




