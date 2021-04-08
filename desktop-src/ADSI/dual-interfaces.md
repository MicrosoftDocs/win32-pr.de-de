---
title: Duale Schnittstellen (ADSI)
description: Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden von ADSI-Objekten eines Anbieters zuzugreifen.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730185"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="e9f17-103">Duale Schnittstellen (ADSI)</span><span class="sxs-lookup"><span data-stu-id="e9f17-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="e9f17-104">Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden von ADSI-Objekten eines Anbieters zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e9f17-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="e9f17-105">Eine schreibgeschützte Eigenschaft wird einem Schnittstellen Eintrag im Formular **get \_ <PropertyName>** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e9f17-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="e9f17-106">Eine Eigenschaft mit Lese-/Schreibzugriff wird zwei Schnittstellen Einträgen im Formular **get \_ <PropertyName>** und **Put \_ <PropertyName>** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e9f17-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="e9f17-107">Alle Methoden einer COM-Schnittstelle müssen folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="e9f17-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="e9f17-108">Gibt einen HRESULT-Wert zurück, der den Erfolg oder Misserfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="e9f17-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="e9f17-109">Der **HRESULT** -Typ wird in der com-Spezifikation erläutert.</span><span class="sxs-lookup"><span data-stu-id="e9f17-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="e9f17-110">Gibt bei Aufrufen von **QueryInterface** **E \_ nointerface** für nicht implementierte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="e9f17-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="e9f17-111">Gibt **E \_ notimpl** für nicht implementierte Methoden für Schnittstellen zurück, die anderweitig implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9f17-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="e9f17-112">Die Rückgabe der E ADS-Eigenschaft wird für nicht unterstützte Schnittstelleneigenschaften **\_ \_ \_ nicht \_ unterstützt** .</span><span class="sxs-lookup"><span data-stu-id="e9f17-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="e9f17-113">Um die Kompatibilität mit Automatisierungs Controllern beizubehalten, sollten alle Parameter und Rückgabe Typen in der Teilmenge liegen, die durch den Datentyp "Automation Variant" definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e9f17-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="e9f17-114">Weitere Informationen finden Sie unter **Variant** und **VARIANTARG** im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e9f17-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="e9f17-115">Ein Anbieter Active Directory-Objekt kann Schnittstellen verfügbar machen, die andere Datentypen als die in der **Variant** -Teilmenge verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9f17-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="e9f17-116">Automatisierungs Controller wie Visual Basic können diese Schnittstellen jedoch nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9f17-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="e9f17-117">Die meisten ADSI-Anbieter Schnittstellen werden von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) abgeleitet und können als **IDispatch** -Schnittstellen Zeiger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9f17-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="e9f17-118">Die ADSI-Schnittstellen [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)und [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) werden jedoch nicht von **IDispatch** abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e9f17-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 