---
description: Video Farbquelle
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Video Farbquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216777"
---
# <a name="video-color-source"></a><span data-ttu-id="e1bd9-103">Video Farbquelle</span><span class="sxs-lookup"><span data-stu-id="e1bd9-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="e1bd9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-104">\[Deprecated.</span></span> <span data-ttu-id="e1bd9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e1bd9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1bd9-106">Die Video Farbquelle erstellt ein kontinuierliches Video Bild mit einer voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="e1bd9-107">Klassen-ID (CLSID): **{0cfdd070-581a-11d2-9ee6-006008039e37}**</span><span class="sxs-lookup"><span data-stu-id="e1bd9-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="e1bd9-108">CLSID-Variablen Name: **CLSID \_ ColorSource**</span><span class="sxs-lookup"><span data-stu-id="e1bd9-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="e1bd9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1bd9-109">Properties</span></span>



| <span data-ttu-id="e1bd9-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1bd9-110">Property</span></span> | <span data-ttu-id="e1bd9-111">type</span><span class="sxs-lookup"><span data-stu-id="e1bd9-111">Type</span></span>      | <span data-ttu-id="e1bd9-112">Standard</span><span class="sxs-lookup"><span data-stu-id="e1bd9-112">Default</span></span> | <span data-ttu-id="e1bd9-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1bd9-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="e1bd9-114">Codes</span><span class="sxs-lookup"><span data-stu-id="e1bd9-114">"Color"</span></span>  | <span data-ttu-id="e1bd9-115">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1bd9-115">**DWORD**</span></span> | <span data-ttu-id="e1bd9-116">0</span><span class="sxs-lookup"><span data-stu-id="e1bd9-116">0</span></span>       | <span data-ttu-id="e1bd9-117">Gibt die zu Generier gende Farbe an.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-117">Specifies the color to generate.</span></span> <span data-ttu-id="e1bd9-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1bd9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1bd9-119">Remarks</span></span>

<span data-ttu-id="e1bd9-120">Die Video Farb Quelle wird mit Quell Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="e1bd9-121">Erstellen Sie zunächst ein neues Quell Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-121">First, create a new source object.</span></span> <span data-ttu-id="e1bd9-122">Legen Sie dann die untergeordnete GUID des Quell Objekts auf CLSID \_ ColorSource fest, indem Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="e1bd9-123">Um die Farbe festzulegen, erstellen Sie ein [Eigenschaften Setter](property-setter.md) -Objekt, und wenden Sie die Color-Eigenschaft zur Zeit 0 (null) an.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="e1bd9-124">Der Wert dieser Eigenschaft ist eine hexadezimale Zahl im Format *0xaarrggbb*, wobei *AA* der Alpha Wert, *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="e1bd9-125">Alpha Werte reichen von 0x00 (transparent) bis 0xFF (undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="e1bd9-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="e1bd9-126">Die-Eigenschaft ist statisch und muss zum Zeitpunkt 0 (null) angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="e1bd9-127">Wenn Sie den Alpha Wert nicht angeben, wird der Wert standardmäßig auf 0 (null) (transparent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="e1bd9-128">In einem 32-Bit-Color-Videoprojekt bewirkt dies, dass Übergänge oder Effekte, bei denen Alpha verwendet wird, um die Video Farb Quelle als vollständig transparent darzustellen.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="e1bd9-129">Um sicher zu sein, geben Sie immer das Alpha an.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="e1bd9-130">Beispielsweise ist " **0xFF000000**" ein undurchsichtiges Schwarzes.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="e1bd9-131">Im folgenden Codebeispiel wird gezeigt, wie dieses-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="e1bd9-132">Weitere Informationen zur Verwendung von [**ipropertysetter**](ipropertysetter.md)finden Sie unter [Festlegen von Eigenschaften für Effekte und Übergänge](setting-properties-on-effects-and-transitions.md):</span><span class="sxs-lookup"><span data-stu-id="e1bd9-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="e1bd9-133">Das folgende Beispiel zeigt die XML-Darstellung des-Objekts, das im vorherigen Beispiel erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1bd9-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="e1bd9-134">In diesem Fall unterstützt das [**param**](param-element.md) -Element keine oder [**lineare**](linear-element.md) Elemente, da das Objekt dynamische Eigenschaften nicht [**unterstützt:**](at-element.md)</span><span class="sxs-lookup"><span data-stu-id="e1bd9-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



