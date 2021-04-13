---
description: Aktualisiert den ursprünglichen Zustand eines Objekts. beispielsweise eine Textur oder ein Shader.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine4:: UpdateObject-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481251"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="3f686-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4:: UpdateObject-Methode</span><span class="sxs-lookup"><span data-stu-id="3f686-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="3f686-104">Aktualisiert den ursprünglichen Zustand eines Objekts. beispielsweise eine Textur oder ein Shader.</span><span class="sxs-lookup"><span data-stu-id="3f686-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f686-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f686-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="3f686-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f686-106">Parameters</span></span>

<span data-ttu-id="3f686-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="3f686-107">*objectAddress* </span></span>  
<span data-ttu-id="3f686-108">Die ID des zu aktualisierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="3f686-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="3f686-109">*Größe* </span><span class="sxs-lookup"><span data-stu-id="3f686-109">*size* </span></span>  
<span data-ttu-id="3f686-110">Die Größe der Update Nutzlast in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3f686-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="3f686-111">*count1- \_ Puffer* </span><span class="sxs-lookup"><span data-stu-id="3f686-111">*count1\_buffer* </span></span>  
<span data-ttu-id="3f686-112">Die Update Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="3f686-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f686-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f686-113">Return value</span></span>

<span data-ttu-id="3f686-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3f686-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f686-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f686-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f686-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f686-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3f686-117">Header</span><span class="sxs-lookup"><span data-stu-id="3f686-117">Header</span></span></p></td><td><span data-ttu-id="3f686-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3f686-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3f686-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f686-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3f686-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="3f686-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 
