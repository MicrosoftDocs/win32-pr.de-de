---
description: Übersicht über die com-Bibliothek und Hinweise zur Verwendung von Tablet PC-Technologie Abschnitten des Windows Vista SDK.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Verwenden der com-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343279"
---
# <a name="using-the-com-library"></a><span data-ttu-id="7016c-103">Verwenden der com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7016c-103">Using the COM Library</span></span>

<span data-ttu-id="7016c-104">Die Referenz zur Tablet PC-verwalteten Bibliothek finden Sie im Abschnitt "reguläre Referenz zur Windows Vista SDK-Klassenbibliothek".</span><span class="sxs-lookup"><span data-stu-id="7016c-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="7016c-105">Sie stellt ein Objektmodell für Microsoft Visual C++ bereit.</span><span class="sxs-lookup"><span data-stu-id="7016c-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="7016c-106">Die Mehrzahl der Objekte in der com-Bibliothek sind identisch mit denen in der von Tablet PC verwalteten API.</span><span class="sxs-lookup"><span data-stu-id="7016c-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="7016c-107">Die com-API enthält jedoch einige Mitglieder zusätzlich zu den in der verwalteten API gefundenen Membern aufgrund von Unterschieden zwischen der standardmäßigen Microsoft Win32-Umgebung und der Microsoft .net frameworksoftware Development Kit (SDK)-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="7016c-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="7016c-108">Beispielsweise werden die Objekte inkrechteck und inktransform in com verwendet, das FrameworkSDK bietet jedoch eine native Implementierung für die [**inkrechteck-Klasse**](inkrectangle-class.md) und die [**inktransform-Klasse**](inktransform-class.md) , die die Notwendigkeit dieser Objekte in der von Tablet PC Platform verwalteten API entfällt.</span><span class="sxs-lookup"><span data-stu-id="7016c-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="7016c-109">Die Objekte in der com-API und den Freihand-Steuerelementen sind nicht für die Verwendung in ASP (Active Server Pages) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="7016c-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="7016c-110">Arbeiten mit Sammlungen</span><span class="sxs-lookup"><span data-stu-id="7016c-110">Working with Collections</span></span>

<span data-ttu-id="7016c-111">Wenn Sie einen **null** -Wert als Index an eine der Auflistungs Objekte in der com-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argument Werte bei der Erstellung in 0 umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7016c-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="7016c-112">Die Eigenschaft " **\_ netwenum** " ist in der IDL-Definition (Interface Definition Language) für die Sammlungs Schnittstellen als eingeschränkt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7016c-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="7016c-113">Verwenden Sie in C++ eine- `For...` Schleife, um eine Auflistung zu durchlaufen, indem Sie zuerst die Länge der Auflistung abrufen.</span><span class="sxs-lookup"><span data-stu-id="7016c-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="7016c-114">Im folgenden Beispiel wird gezeigt, wie die Striche eines [**InkDisp**](inkdisp-class.md) -Objekts durchlaufen werden `pInk` .</span><span class="sxs-lookup"><span data-stu-id="7016c-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a><span data-ttu-id="7016c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7016c-115">Parameters</span></span>

<span data-ttu-id="7016c-116">Wenn Sie VT \_ Empty oder VT \_ null als Index an eine der Auflistungs Objekte in der com-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argument Werte bei der Erstellung in 0 umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7016c-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="7016c-117">Verwenden von IDispatch</span><span class="sxs-lookup"><span data-stu-id="7016c-117">Using IDispatch</span></span>

<span data-ttu-id="7016c-118">Um die Leistung zu verbessern, unterstützt die Tablet PC Platform com Application Programming Interface (API) das Aufrufen `IDispatchImpl::Invoke` von mit einer DISPPARAMS-Struktur mit benannten Argumenten nicht.</span><span class="sxs-lookup"><span data-stu-id="7016c-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="7016c-119">`IDispatchImpl::GetIDsOfNames`Wird auch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7016c-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="7016c-120">Verwenden Sie stattdessen `Invoke` mit den in den SDK-Headern angegebenen DispIds.</span><span class="sxs-lookup"><span data-stu-id="7016c-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="7016c-121">Warten auf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7016c-121">Waiting for Events</span></span>

<span data-ttu-id="7016c-122">Die Tablet PC-Umgebung ist multithreaded.</span><span class="sxs-lookup"><span data-stu-id="7016c-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="7016c-123">Weitere Informationen finden Sie in der com-Dokumentation zum Multithreading.</span><span class="sxs-lookup"><span data-stu-id="7016c-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="7016c-124">Unterstützung für Aggregation</span><span class="sxs-lookup"><span data-stu-id="7016c-124">Support for Aggregation</span></span>

<span data-ttu-id="7016c-125">Die Aggregation wurde nur für das [InkEdit](inkedit-control-reference.md) -Steuerelement, das [InkPicture](inkpicture-control-reference.md) -Steuerelement, das [**InkDisp**](inkdisp-class.md) -Objekt und das [**InkOverlay**](inkoverlay-class.md) -Objekt getestet.</span><span class="sxs-lookup"><span data-stu-id="7016c-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="7016c-126">Die Aggregation wurde nicht für andere Steuerelemente und Objekte in der Bibliothek getestet.</span><span class="sxs-lookup"><span data-stu-id="7016c-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="7016c-127">C++</span><span class="sxs-lookup"><span data-stu-id="7016c-127">C++</span></span>

<span data-ttu-id="7016c-128">Die Verwendung des Tablet PC SDK in C++ erfordert die Verwendung einiger com-Konzepte wie Variant, SAFEARRAY und BSTR.</span><span class="sxs-lookup"><span data-stu-id="7016c-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="7016c-129">In diesem Abschnitt wird beschrieben, wie Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7016c-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="7016c-130">Variant und SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="7016c-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="7016c-131">Die VARIANT-Struktur wird für die Kommunikation zwischen COM-Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7016c-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="7016c-132">Im Wesentlichen handelt es sich bei der VARIANT-Struktur um einen Container für eine große Union, die viele Datentypen enthält.</span><span class="sxs-lookup"><span data-stu-id="7016c-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="7016c-133">Der Wert im ersten Element der Struktur, VT, beschreibt, welche der Union-Member gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7016c-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="7016c-134">Wenn Sie Informationen in einer VARIANT-Struktur erhalten, überprüfen Sie das VT-Element, um herauszufinden, welches Mitglied gültige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7016c-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="7016c-135">Wenn Sie Informationen mithilfe einer VARIANT-Struktur senden, legen Sie auf ähnliche Weise fest, dass VT das Unionmember enthält, das die Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7016c-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="7016c-136">Bevor Sie die-Struktur verwenden, initialisieren Sie Sie, indem Sie die VariantInit com-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7016c-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="7016c-137">Wenn die Struktur fertig ist, löschen Sie Sie, bevor der Speicher, der die Variante enthält, durch Aufrufen von VariantClear freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7016c-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="7016c-138">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Variant-und VARIANTARG-Datentypen](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="7016c-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="7016c-139">Die SAFEARRAY-Struktur wird als Möglichkeit bereitgestellt, mit Arrays in com sicher zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7016c-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="7016c-140">Das anvariant-Feld ist ein Zeiger auf ein SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="7016c-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="7016c-141">Verwenden Sie Funktionen wie z. b. safearraykreatevector, safearrayaccessdata und safearrayunaccessdata, um ein SAFEARRAY in einer Variante zu erstellen und auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="7016c-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="7016c-142">Weitere Informationen zum SAFEARRAY-Datentyp finden Sie unter [SAFEARRAY-Datentyp](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="7016c-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="7016c-143">In diesem C++-Beispiel wird ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) - `pInkStrokeDisp` Objekt in einem [**InkDisp**](inkdisp-class.md) -Objekt `pInk` aus einem Array von Punktdaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="7016c-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a><span data-ttu-id="7016c-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="7016c-144">BSTR</span></span>

<span data-ttu-id="7016c-145">Das unterstützte Zeichen folgen Format für com ist BSTR.</span><span class="sxs-lookup"><span data-stu-id="7016c-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="7016c-146">Ein BSTR weist einen Zeiger auf eine NULL-terminierte Zeichenfolge auf, enthält jedoch auch die Länge der Zeichenfolge (in Bytes, die das Abschluss Zeichen nicht zählt), die in den 4 Bytes unmittelbar vor dem ersten Zeichen der Zeichenfolge gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7016c-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="7016c-147">Weitere Informationen zu BSTR finden Sie unter [BSTR-Datentyp](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="7016c-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="7016c-148">In diesem C++-Beispiel wird gezeigt, wie die Faktoid für einen [**inkrecognizercontext**](inkrecognizercontext-class.md) mithilfe eines BSTR festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7016c-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
