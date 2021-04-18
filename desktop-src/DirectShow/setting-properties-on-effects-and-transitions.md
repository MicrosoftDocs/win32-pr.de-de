---
description: Festlegen von Eigenschaften für Effekte und Übergänge
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Festlegen von Eigenschaften für Effekte und Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344155"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="e1920-103">Festlegen von Eigenschaften für Effekte und Übergänge</span><span class="sxs-lookup"><span data-stu-id="e1920-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="e1920-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="e1920-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e1920-105">Viele [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) haben Auswirkungen und Übergängen unterstützen Eigenschaften, die ihr Verhalten steuern.</span><span class="sxs-lookup"><span data-stu-id="e1920-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="e1920-106">Eine Anwendung kann den Wert einer Eigenschaft mithilfe der [**ipropertysetter**](ipropertysetter.md) -Schnittstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="e1920-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="e1920-107">Das zugrunde liegende Effekt-oder Übergangs Objekt muss **IDispatch** zum Festlegen der Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e1920-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="e1920-108">Mit Video Effekten und-Übergängen kann die Anwendung einen Wertebereich festlegen, der sich im Laufe der Zeit ändert.</span><span class="sxs-lookup"><span data-stu-id="e1920-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="e1920-109">(Sie können z. b. einen zurücksetzenübergang festlegen, um über den Frame hin und her zu wechseln.) Mit Audioeffekten ist der Wert der Eigenschaft statisch und kann sich im Laufe der Zeit nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e1920-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="e1920-110">Die einzige Ausnahme ist der [volumeumschlags](volume-envelope-effect.md) Effekt, der eine dynamische Eigenschaft für die Volumeebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1920-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="e1920-111">Führen Sie die folgenden Schritte aus, um eine Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e1920-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="e1920-112">Erstellen Sie eine Instanz des Eigenschaften Setters (CLSID \_ propertysetter).</span><span class="sxs-lookup"><span data-stu-id="e1920-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="e1920-113">Füllen Sie die Struktur von [**Dexter \_ param**](dexter-param.md) -und [**Dexter- \_ Werten**](dexter-value.md) mit den Eigenschaften Daten aus.</span><span class="sxs-lookup"><span data-stu-id="e1920-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="e1920-114">Diese Strukturen werden im folgenden erläutert.</span><span class="sxs-lookup"><span data-stu-id="e1920-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="e1920-115">Übergeben Sie die " [**Dexter \_ param**](dexter-param.md) "-und " [**Dexter \_ value**](dexter-value.md) "-Strukturen an die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e1920-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="e1920-116">Wiederholen Sie die Schritte 2 und 3 für jede Eigenschaft, die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="e1920-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="e1920-117">Übergeben Sie den [**ipropertysetter**](ipropertysetter.md) -Schnittstellen Zeiger an die [**iamtimelineobj:: setpropertysetter**](iamtimelineobj-setpropertysetter.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e1920-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="e1920-118">Die " [**Dexter \_ param**](dexter-param.md) "-Struktur gibt an, welche Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e1920-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="e1920-119">Sie enthält die folgenden Member.</span><span class="sxs-lookup"><span data-stu-id="e1920-119">It contains the following members.</span></span>

-   <span data-ttu-id="e1920-120">**Name**: Name der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1920-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="e1920-121">**DISPID**: reserviert, muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e1920-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="e1920-122">**nvalues**: Anzahl der Werte</span><span class="sxs-lookup"><span data-stu-id="e1920-122">**nValues**: Number of values</span></span>

<span data-ttu-id="e1920-123">Die \_ Wert Struktur von "Dexter" gibt den Wert einer Eigenschaft zu einem bestimmten Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="e1920-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="e1920-124">Sie enthält die folgenden Member.</span><span class="sxs-lookup"><span data-stu-id="e1920-124">It contains the following members.</span></span>

-   <span data-ttu-id="e1920-125">**v**: Variant-Typ, der einen neuen Wert für die-Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="e1920-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="e1920-126">Der **VT** -Member dieser Variante definiert den Datentyp der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e1920-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="e1920-127">Weitere Informationen zum **Variant** -Typ finden Sie in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e1920-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="e1920-128">**RT**: Verweis Zeit, wenn die Eigenschaft diesen Wert annimmt, relativ zur Startzeit des Effekts oder Übergangs.</span><span class="sxs-lookup"><span data-stu-id="e1920-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="e1920-129">Die Startzeit des Effekts oder Übergangs bezieht sich auf die Startzeit des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="e1920-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="e1920-130">**dwinterp**: Flag, das angibt, wie die-Eigenschaft vom vorherigen Wert in den neuen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e1920-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="e1920-131">Mit dem dexterf- \_ springflag springt die Eigenschaft zum angegebenen Zeitpunkt sofort in den neuen Wert.</span><span class="sxs-lookup"><span data-stu-id="e1920-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="e1920-132">Beim dexterf- \_ interinterpolate-Flag wird die-Eigenschaft linear aus dem vorherigen Wert interpoliert.</span><span class="sxs-lookup"><span data-stu-id="e1920-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="e1920-133">Wenn Sie das **VT** -Element auf VT \_ BSTR festlegen, führt der Eigenschaften Setter alle notwendigen Konvertierungen aus.</span><span class="sxs-lookup"><span data-stu-id="e1920-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="e1920-134">Fügen Sie für Gleit Komma Werte die führende Null vor der Dezimalstelle ein.</span><span class="sxs-lookup"><span data-stu-id="e1920-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="e1920-135">Beispielsweise 0,3, nicht. 3.</span><span class="sxs-lookup"><span data-stu-id="e1920-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="e1920-136">Anwendungen sollten die Konvertierung von **BSTR**-s in numerische Werte vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e1920-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="e1920-137">Wenn die Eigenschaft einen numerischen Wert aufweist, verwenden Sie den entsprechenden numerischen **Variant** -Typ.</span><span class="sxs-lookup"><span data-stu-id="e1920-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="e1920-138">Der Wert einer Eigenschaft kann sich im Laufe der Zeit ändern, sodass die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode eine einzelne " [**Dexter \_ param**](dexter-param.md) "-Struktur und einen Zeiger auf ein Array von " [**Dexter \_ value**](dexter-value.md) "-Strukturen annimmt.</span><span class="sxs-lookup"><span data-stu-id="e1920-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="e1920-139">Das Array definiert einen Satz zeitbasierter Werte für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e1920-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="e1920-140">Die Elemente des Arrays müssen sich in aufsteigender Zeitreihen Folge befinden, und der **nvalues** -Member der "Dexter \_ Param"-Struktur muss der Länge des Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e1920-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="e1920-141">Im folgenden Codebeispiel werden Eigenschafts Daten für den [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1920-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="e1920-142">Der Code wird auf 120 festgelegt, wodurch ein Oval-zurücksetzen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e1920-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="e1920-143">Die Verweis Zeit wird auf NULL festgelegt, was den Beginn des Übergangs angibt.</span><span class="sxs-lookup"><span data-stu-id="e1920-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="e1920-144">**Dynamisch veränderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="e1920-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="e1920-145">Nachdem Sie ein Video Bearbeitungs Projekt gerenkt haben, ist es möglich, die Eigenschaften eines Effekts oder Übergangs Objekts während der Ausführung des Diagramms zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e1920-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="e1920-146">Dies ist jedoch nur möglich, wenn Sie Eigenschaften für dieses Objekt festlegen, bevor die Anwendung den Namen " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md)" hat.</span><span class="sxs-lookup"><span data-stu-id="e1920-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="e1920-147">Wenn dies der Fall ist, können Sie [**iamtimelineobj:: getpropertysetter**](iamtimelineobj-getpropertysetter.md) für den Effekt oder Übergang aufrufen, die Eigenschaften löschen oder ändern, und die Änderungen werden dynamisch durchgeführt, wenn das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1920-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="e1920-148">Während der Änderung können visuelle Anomalien auftreten, daher wird dies nur für die Vorschau empfohlen.</span><span class="sxs-lookup"><span data-stu-id="e1920-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="e1920-149">Ändern Sie die Eigenschaften nicht, während Sie das Projekt in eine Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="e1920-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="e1920-150">Wenn Sie keine Eigenschaften für den Effekt oder das Übergangs Objekt festgelegt haben, bevor Sie **connectfrontend** aufgerufen haben, können Sie ihm während der Ausführung des Diagramms keine Eigenschaften hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e1920-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1920-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1920-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1920-152">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="e1920-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



