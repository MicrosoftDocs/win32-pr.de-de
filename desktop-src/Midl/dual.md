---
title: dual-Attribut
description: Das Dual-Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über IDispatch und direkt über den VTBL verfügbar macht.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- Dual Attribute-Mittel l
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948722"
---
# <a name="dual-attribute"></a><span data-ttu-id="eb101-104">dual-Attribut</span><span class="sxs-lookup"><span data-stu-id="eb101-104">dual attribute</span></span>

<span data-ttu-id="eb101-105">Das **Dual** -Attribut identifiziert eine Schnittstelle, die Eigenschaften und Methoden über [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und direkt über den VTBL verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="eb101-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="eb101-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb101-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="eb101-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="eb101-108">Gibt eine universell eindeutige Identifikationsnummer für die Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="eb101-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="eb101-109">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="eb101-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="eb101-110">Gibt eine Liste von 0 (null) oder mehr zusätzlichen Mittelwert Attributen an.</span><span class="sxs-lookup"><span data-stu-id="eb101-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="eb101-111">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="eb101-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="eb101-112">Der Name der Schnittstelle, auf die das **Dual** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb101-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb101-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb101-113">Remarks</span></span>

<span data-ttu-id="eb101-114">Schnittstellen, die durch das **Dual** -Attribut identifiziert werden, müssen mit Automation kompatibel sein und von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="eb101-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="eb101-115">Dieses Attribut ist für dispinterfaces nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="eb101-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="eb101-116">Das **Dual** -Attribut erstellt eine Schnittstelle, die sowohl eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle als auch eine Component Object Model (com)-Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="eb101-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="eb101-117">Die ersten sieben Einträge der VTBL für eine duale Schnittstelle sind die sieben Member von **IDispatch**, und die restlichen Einträge sind für den direkten Zugriff auf Member der Dual-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eb101-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="eb101-118">Alle Parameter und Rückgabe Typen, die für Member einer Dual-Schnittstelle angegeben sind, müssen Automatisierungs kompatible Typen sein.</span><span class="sxs-lookup"><span data-stu-id="eb101-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="eb101-119">Alle Member einer Dual-Schnittstelle müssen ein HRESULT als Rückgabewert der Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="eb101-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="eb101-120">Member, z. b. eigenschaftenaccessorfunktionen, die andere Werte zurückgeben müssen, sollten den letzten Parameter als " [**out**](out-idl.md)", " [**retval**](retval.md)" angeben, der einen Ausgabeparameter angibt, der den Wert der Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eb101-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="eb101-121">Außerdem sollten Member, die mehrere Gebiets Schemas unterstützen müssen, einen [**LCID**](lcid.md) -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="eb101-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="eb101-122">Eine duale Schnittstelle ermöglicht sowohl die Geschwindigkeit der direkten VTBL-Bindung als auch die Flexibilität der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Bindung.</span><span class="sxs-lookup"><span data-stu-id="eb101-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="eb101-123">Aus diesem Grund werden zwei Schnittstellen empfohlen, wann immer dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="eb101-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="eb101-124">Wenn Ihre Anwendung auf Objektdaten zugreift, indem Sie *den Zeiger in den Schnittstellen* aufzurufen umwandeln, sollten Sie die VTBL-Zeiger im Objekt anhand ihrer eigenen VTBL-Zeiger überprüfen, um sicherzustellen, dass Sie mit dem entsprechenden Proxy verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="eb101-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="eb101-125">Das Angeben von **Dual** für eine Schnittstelle impliziert, dass die Schnittstelle mit Automation kompatibel ist, sodass sowohl das TYPEFLAG \_ fdual-als auch das TYPEFLAG \_ foleautomation-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eb101-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="eb101-126">Flags</span><span class="sxs-lookup"><span data-stu-id="eb101-126">Flags</span></span>

<span data-ttu-id="eb101-127">TYPEFLAG ( \_ odual), TYPEFLAG \_ foleautomation</span><span class="sxs-lookup"><span data-stu-id="eb101-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="eb101-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb101-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="eb101-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb101-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb101-130">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="eb101-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="eb101-131">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="eb101-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="eb101-132">**LCID**</span><span class="sxs-lookup"><span data-stu-id="eb101-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="eb101-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="eb101-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="eb101-134">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="eb101-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="eb101-135">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="eb101-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="eb101-136">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="eb101-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="eb101-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="eb101-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 