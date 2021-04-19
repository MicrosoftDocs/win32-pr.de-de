---
description: Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Lpfninitroutine-Funktionszeiger (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352958"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="f156c-103">Lpfninitroutine-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="f156c-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="f156c-104">Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f156c-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="f156c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f156c-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="f156c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f156c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f156c-107">*bloading*</span><span class="sxs-lookup"><span data-stu-id="f156c-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="f156c-108">**True** , wenn die dll geladen wird, **false** , wenn die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="f156c-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="f156c-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="f156c-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="f156c-110">Zeiger auf das CLISD des Objekts, das in der [**cfactorytemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) -Element Variablen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f156c-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f156c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f156c-111">Return value</span></span>

<span data-ttu-id="f156c-112">Dieser Funktionszeiger gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f156c-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f156c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f156c-113">Requirements</span></span>



| <span data-ttu-id="f156c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f156c-114">Requirement</span></span> | <span data-ttu-id="f156c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f156c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f156c-116">Header</span><span class="sxs-lookup"><span data-stu-id="f156c-116">Header</span></span><br/> | <dl> <span data-ttu-id="f156c-117"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f156c-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f156c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f156c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f156c-119">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f156c-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




