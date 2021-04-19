---
description: Legt die monikerbindungsflags für den Microsoft Media Foundation http-Byte-Stream fest.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366908"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="addd4-103">Mfpkey \_ http \_ Bytestream- \_ URLMON- \_ \_ Bindungsflags (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="addd4-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="addd4-104">Legt die monikerbindungsflags für den Microsoft Media Foundation http-Byte-Stream fest.</span><span class="sxs-lookup"><span data-stu-id="addd4-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="addd4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="addd4-105">Data type</span></span>

<span data-ttu-id="addd4-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="addd4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="addd4-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="addd4-107">PROPVARIANT member</span></span>

<span data-ttu-id="addd4-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="addd4-108">**ULONG**</span></span>

<span data-ttu-id="addd4-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="addd4-109">VT\_UI4</span></span>

<span data-ttu-id="addd4-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="addd4-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="addd4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="addd4-111">Remarks</span></span>

<span data-ttu-id="addd4-112">Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="addd4-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="addd4-113">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="addd4-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="addd4-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="addd4-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="addd4-115">Der Wert dieser Eigenschaft ist ein bitweises **or** von Flags aus der **bindf** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="addd4-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="addd4-116">Diese Eigenschaft wird nur angewendet, wenn die Eigenschaft [mfpkey \_ http \_ Bytestream \_ enable \_ URLMON](mfpkey-http-bytestream-enable-urlmon.md) auf **Variant \_ true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="addd4-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="addd4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="addd4-117">Requirements</span></span>



| <span data-ttu-id="addd4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="addd4-118">Requirement</span></span> | <span data-ttu-id="addd4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="addd4-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="addd4-120">Header</span><span class="sxs-lookup"><span data-stu-id="addd4-120">Header</span></span><br/> | <dl> <span data-ttu-id="addd4-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="addd4-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="addd4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="addd4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addd4-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="addd4-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
