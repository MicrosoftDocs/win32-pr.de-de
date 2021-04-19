---
description: Die inondelegatingunknown-Schnittstelle ist eine Version von IUnknown, die umbenannt wird, um die Unterstützung für die nicht Delegierung und Delegierung von IUnknown-Schnittstellen im selben com-Objekt zu ermöglichen.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: Inondelegatingunknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370288"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="1d5f4-103">Inondelegatingunknown</span><span class="sxs-lookup"><span data-stu-id="1d5f4-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="1d5f4-104">Die- `INonDelegatingUnknown` Schnittstelle ist eine Version von **IUnknown** , die umbenannt wird, um die Unterstützung für die nicht Delegierung und Delegierung von **IUnknown** -Schnittstellen im gleichen com-Objekt zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5f4-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="1d5f4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d5f4-106">Remarks</span></span>

<span data-ttu-id="1d5f4-107">Führen Sie `INonDelegatingUnknown` die folgenden Schritte aus, um für die mehrfache Vererbung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="1d5f4-108">Leiten Sie die Klasse von einer Schnittstelle ab, z. b. IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="1d5f4-109">Fügen [**Sie \_ Declare IUnknown**](declare-iunknown.md) in die Klassendefinition ein, um Implementierungen von **QueryInterface**, **adressf** und **Release** zu deklarieren, die das äußere unbekannte-Element aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="1d5f4-110">Überschreiben Sie **nondelegatingqueryinterface** , um IMyInterface mit Code wie dem folgenden verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="1d5f4-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1d5f4-111">Deklarieren und implementieren Sie die Element Funktionen von IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="1d5f4-112">Führen Sie `INonDelegatingUnknown` die folgenden Schritte aus, um für die-Schnittstellen zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="1d5f4-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="1d5f4-113">Deklarieren Sie eine von [**cunknown**](cunknown.md)abgeleitete Klasse.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="1d5f4-114">Include [**Declare \_ IUnknown**](declare-iunknown.md) in der Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="1d5f4-115">Überschreiben Sie **nondelegatingqueryinterface** , um IMyInterface mit dem folgenden Code verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="1d5f4-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1d5f4-116">Implementieren Sie die Member-Funktionen von IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="1d5f4-117">Verwenden Sie [**cunknown:: GetOwner**](cunknown-getowner.md) , um auf die com-Objektklasse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="1d5f4-118">Legen Sie in der com-Objektklasse die-Klasse als Friend der com-Objektklasse ab, und deklarieren Sie eine Instanz der-Klasse als Member der com-Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="1d5f4-119">Da Sie den äußeren unbekannten und ein **HRESULT** immer an den [**cunknown**](cunknown.md) -Konstruktor übergeben müssen, können Sie keinen Standardkonstruktor verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="1d5f4-120">Sie müssen die Member-Variable zu einem Zeiger auf die Klasse machen und einen neuen-Befehl in Ihrem Konstruktor erstellen, um Sie tatsächlich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="1d5f4-121">Überschreiben Sie die **nondelegatingqueryinterface** mit folgendem Code:</span><span class="sxs-lookup"><span data-stu-id="1d5f4-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="1d5f4-122">Sie können gemischte Klassen haben, die einige Schnittstellen durch mehrfache Vererbung und einige Schnittstellen durch schsted Klassen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5f4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d5f4-123">Requirements</span></span>



| <span data-ttu-id="1d5f4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d5f4-124">Requirement</span></span> | <span data-ttu-id="1d5f4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1d5f4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5f4-126">Header</span><span class="sxs-lookup"><span data-stu-id="1d5f4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1d5f4-127"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5f4-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d5f4-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d5f4-128">Library</span></span><br/> | <dl> <span data-ttu-id="1d5f4-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5f4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5f4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d5f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5f4-131">**COM-Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1d5f4-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




