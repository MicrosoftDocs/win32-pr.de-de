---
description: Ermöglicht dem Microsoft Media Foundation http-Bytestream, URL-Moniker (auch Urlmon genannt) zu verwenden.
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359256"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="ef325-103">Mfpkey \_ http \_ Bytestream \_ enable \_ URLMON (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ef325-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="ef325-104">Ermöglicht dem Microsoft Media Foundation http-Bytestream, URL-Moniker (auch *URLMON* genannt) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef325-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="ef325-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ef325-105">Data type</span></span>

<span data-ttu-id="ef325-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="ef325-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ef325-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="ef325-107">PROPVARIANT member</span></span>

<span data-ttu-id="ef325-108">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ef325-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="ef325-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="ef325-109">VT\_BOOL</span></span>

<span data-ttu-id="ef325-110">**Boolesche Werte**</span><span class="sxs-lookup"><span data-stu-id="ef325-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ef325-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef325-111">Remarks</span></span>

<span data-ttu-id="ef325-112">Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef325-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="ef325-113">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="ef325-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="ef325-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="ef325-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="ef325-115">Wenn der Wert **Variant \_ true** ist, verwendet der http-Bytestream Urlmon für den HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="ef325-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="ef325-116">Andernfalls verwendet der Bytestream WinHTTP, wenn der Wert **Variant \_ false** ist.</span><span class="sxs-lookup"><span data-stu-id="ef325-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="ef325-117">Der Standardwert ist **Variant \_ true** für Windows Store-Apps und **Variant \_ false** für Windows-Desktop Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ef325-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef325-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef325-118">Requirements</span></span>



| <span data-ttu-id="ef325-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef325-119">Requirement</span></span> | <span data-ttu-id="ef325-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ef325-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef325-121">Header</span><span class="sxs-lookup"><span data-stu-id="ef325-121">Header</span></span><br/> | <dl> <span data-ttu-id="ef325-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef325-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef325-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef325-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef325-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ef325-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
