---
title: Bewährte Methoden für die Verwendung von sicheren Arrays
description: Viele Schnittstellen Methoden der Microsoft UI Automation \ 32; API übernimmt Argumente, die als sichere Arrays bezeichnet werden, des SAFEARRAY-Datentyps. In diesem Thema werden die bewährten Methoden für die Verwendung von sicheren Arrays in Benutzeroberflächenautomatisierungs-Anwendungen beschrieben.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Benutzeroberflächen Automatisierung, sichere Arrays
- Benutzeroberflächen Automatisierung, Anbieter
- Benutzeroberflächen Automatisierung, Clients
- Automatisierung der Benutzeroberfläche, umrechnen zwischen Datentypen
- Clients, sichere Arrays
- Anbieter, Benutzeroberflächen Automatisierung
- sichere Arrays
- Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337453"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="660e4-112">Bewährte Methoden für die Verwendung von sicheren Arrays</span><span class="sxs-lookup"><span data-stu-id="660e4-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="660e4-113">Viele Schnittstellen Methoden der Microsoft UI Automation API akzeptieren Argumente, die als sichere Arrays bezeichnet werden, des [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) -Datentyps.</span><span class="sxs-lookup"><span data-stu-id="660e4-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="660e4-114">In diesem Thema werden die bewährten Methoden für die Verwendung von sicheren Arrays in Benutzeroberflächenautomatisierungs-Anwendungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="660e4-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="660e4-115">Clients</span><span class="sxs-lookup"><span data-stu-id="660e4-115">Clients</span></span>

<span data-ttu-id="660e4-116">Alle sicheren Arrays, die mit den Benutzeroberflächenautomatisierungs-Client-API-Methoden verwendet werden, sind null basierte, eindimensionale Arrays.</span><span class="sxs-lookup"><span data-stu-id="660e4-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="660e4-117">Um ein sicheres Array für eine Benutzeroberflächenautomatisierungs-Client Methode zu erstellen, verwenden Sie die [**safearraykreatevector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) -Funktion, und verwenden Sie zum Lesen und Schreiben in ein sicheres Array die Funktionen [**safearraygetelement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) und [**safearrayputelement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="660e4-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="660e4-118">Wenn Sie die Verwendung eines sicheren Arrays abgeschlossen haben, sollten Sie es immer mit der [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) -Funktion zerstören, unabhängig davon, ob Sie das sichere Array erstellt oder von einer Benutzeroberflächenautomatisierungs-Client Methode empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="660e4-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="660e4-119">Mehrere Methoden zur Benutzeroberflächen Automatisierung, einschließlich Eigenschaften Abruf Methoden wie z. b. [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), rufen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)s ab, die [**Punkt**](/previous-versions//dd162805(v=vs.85)) -oder [**uiarect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) -Strukturen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="660e4-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="660e4-120">Ein **Punkt** wird in eine **Variante** als sicheres Array von Doubles (VT \_ R8) mit dem **x** -Member an Index 0 und dem **y** -Element bei Index 1 verpackt.</span><span class="sxs-lookup"><span data-stu-id="660e4-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="660e4-121">Analog dazu wird **ein uiarect** in eine **Variante** als sicheres Array von Double-Elementen mit den Elementen **left**, **Top**, **Width** und **height** bei den Indizes 0 bis 3 verpackt.</span><span class="sxs-lookup"><span data-stu-id="660e4-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="660e4-122">Für ein Array von **uiarect** -Strukturen enthält das sichere Array ein sequenzielles Array von vier Doubles für jeden **uiarect**.</span><span class="sxs-lookup"><span data-stu-id="660e4-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="660e4-123">Die Elemente **left**, **Top**, **Width** und **height** des ersten **uiarect** belegen den Index 0 bis 3, die Elemente des zweiten Rechtecks belegen den Index 4 bis 7 usw.</span><span class="sxs-lookup"><span data-stu-id="660e4-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="660e4-124">Die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle umfasst die folgenden Methoden für die Typumwandlung zwischen [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) und verschiedenen anderen Datentypen.</span><span class="sxs-lookup"><span data-stu-id="660e4-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="660e4-125">Methode</span><span class="sxs-lookup"><span data-stu-id="660e4-125">Method</span></span>                                                                                               | <span data-ttu-id="660e4-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="660e4-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="660e4-127">**Iuiautomation:: intnativearrayto SAFEARRAY**</span><span class="sxs-lookup"><span data-stu-id="660e4-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="660e4-128">Konvertiert ein Array von ganzen Zahlen in ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="660e4-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="660e4-129">**Iuiautomation:: inzafearraytonativearray**</span><span class="sxs-lookup"><span data-stu-id="660e4-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="660e4-130">Konvertiert ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von ganzen Zahlen in ein Array.</span><span class="sxs-lookup"><span data-stu-id="660e4-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="660e4-131">**Iuiautomation:: safearraytor ectnativearray**</span><span class="sxs-lookup"><span data-stu-id="660e4-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="660e4-132">Konvertiert ein [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) , das Rechteck Koordinaten enthält, in ein Array vom Typ " **Rect**".</span><span class="sxs-lookup"><span data-stu-id="660e4-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="660e4-133">Anbieter</span><span class="sxs-lookup"><span data-stu-id="660e4-133">Providers</span></span>

<span data-ttu-id="660e4-134">Ein Anbieter muss eine Reihe von Schnittstellen Methoden implementieren, die von der Benutzeroberflächen Automatisierung aufgerufen werden, um Informationen vom Anbieter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="660e4-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="660e4-135">Viele Male bestehen diese Informationen aus einem Array von Werten.</span><span class="sxs-lookup"><span data-stu-id="660e4-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="660e4-136">Zum Zurückgeben eines Arrays an die Benutzeroberflächen Automatisierung muss der Anbieter das Array in eine [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) -Struktur packen.</span><span class="sxs-lookup"><span data-stu-id="660e4-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="660e4-137">Die Array Elemente müssen den erwarteten Datentyp aufweisen und müssen in der erwarteten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="660e4-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="660e4-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="660e4-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="660e4-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="660e4-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="660e4-140">Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="660e4-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="660e4-141">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="660e4-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 