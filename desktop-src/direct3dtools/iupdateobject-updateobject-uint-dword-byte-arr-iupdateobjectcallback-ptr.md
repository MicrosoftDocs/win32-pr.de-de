---
description: Eine Anforderung zum Aktualisieren des Anfangs Zustands eines Objekts. beispielsweise eine Textur oder ein Shader.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iupdateobject:: UpdateObject-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481998"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="bcb25-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Iupdateobject:: UpdateObject-Methode</span><span class="sxs-lookup"><span data-stu-id="bcb25-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="bcb25-104">Eine Anforderung zum Aktualisieren des Anfangs Zustands eines Objekts. beispielsweise eine Textur oder ein Shader.</span><span class="sxs-lookup"><span data-stu-id="bcb25-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcb25-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="bcb25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcb25-106">Parameters</span></span>

<span data-ttu-id="bcb25-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="bcb25-107">*objectAddress* </span></span>  
<span data-ttu-id="bcb25-108">Die ID des zu aktualisierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="bcb25-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="bcb25-109">*Größe* </span><span class="sxs-lookup"><span data-stu-id="bcb25-109">*size* </span></span>  
<span data-ttu-id="bcb25-110">Die Größe der Update Nutzlast in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bcb25-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="bcb25-111">*count1- \_ Puffer* </span><span class="sxs-lookup"><span data-stu-id="bcb25-111">*count1\_buffer* </span></span>  
<span data-ttu-id="bcb25-112">Die Update Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="bcb25-112">The update payload.</span></span>

<span data-ttu-id="bcb25-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="bcb25-113">*pCallback* </span></span>  
<span data-ttu-id="bcb25-114">Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass das Objekt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bcb25-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcb25-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcb25-115">Return value</span></span>

<span data-ttu-id="bcb25-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bcb25-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bcb25-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bcb25-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb25-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcb25-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bcb25-119">Header</span><span class="sxs-lookup"><span data-stu-id="bcb25-119">Header</span></span></p></td><td><span data-ttu-id="bcb25-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bcb25-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="bcb25-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb25-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="bcb25-122">**Iupdateobject**</span><span class="sxs-lookup"><span data-stu-id="bcb25-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
