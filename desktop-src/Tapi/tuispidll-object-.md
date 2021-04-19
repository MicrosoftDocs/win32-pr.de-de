---
description: Das tuispidll- \_ Objekt wird unten definiert.
ms.assetid: bc0f876d-2443-4c3c-b723-3f82dc6bf849
title: TUISPIDLL_OBJECT_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a4711478b98f1ab4983fd8c83a59772e5b370e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366772"
---
# <a name="tuispidll_object_"></a><span data-ttu-id="c75aa-103">tuispidll- \_ Objekt\_</span><span class="sxs-lookup"><span data-stu-id="c75aa-103">TUISPIDLL\_OBJECT\_</span></span>

<dl> <dt>

<span data-ttu-id="c75aa-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**tuispidll- \_ Objekt ( \_ LineID)**</span><span class="sxs-lookup"><span data-stu-id="c75aa-104"><span id="TUISPIDLL_OBJECT_LINEID"></span><span id="tuispidll_object_lineid"></span>**TUISPIDLL\_OBJECT\_LINEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c75aa-105">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c75aa-105">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="c75aa-106">*dwobjectid* ist eine zeilige Geräte-ID (dwendviceid).</span><span class="sxs-lookup"><span data-stu-id="c75aa-106">*dwObjectID* is a line device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c75aa-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**tuispidll- \_ Objekt \_ phoneid**</span><span class="sxs-lookup"><span data-stu-id="c75aa-107"><span id="TUISPIDLL_OBJECT_PHONEID"></span><span id="tuispidll_object_phoneid"></span>**TUISPIDLL\_OBJECT\_PHONEID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c75aa-108">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c75aa-108">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="c75aa-109">*dwobjectid* ist eine Telefongeräte-ID (dwendviceid).</span><span class="sxs-lookup"><span data-stu-id="c75aa-109">*dwObjectID* is a phone device identifier (dwDeviceID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c75aa-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**"tuispidll \_ Object \_ ProviderID"**</span><span class="sxs-lookup"><span data-stu-id="c75aa-110"><span id="TUISPIDLL_OBJECT_PROVIDERID"></span><span id="tuispidll_object_providerid"></span>**TUISPIDLL\_OBJECT\_PROVIDERID**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c75aa-111">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c75aa-111">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="c75aa-112">*dwobjectid* ist ein dauerhafter Anbieter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c75aa-112">*dwObjectID* is a permanent provider identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c75aa-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**tuispidll- \_ Objekt \_ dialoginstance**</span><span class="sxs-lookup"><span data-stu-id="c75aa-113"><span id="TUISPIDLL_OBJECT_DIALOGINSTANCE"></span><span id="tuispidll_object_dialoginstance"></span>**TUISPIDLL\_OBJECT\_DIALOGINSTANCE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="c75aa-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c75aa-114">0x00000004</span></span> 
</dt> <dt>



<span data-ttu-id="c75aa-115">*dwobjectid* ist ein Dialog Instanzhandle (entweder hdrvdialoginstance oder htapidialoginstance, abhängig vom Kontext).</span><span class="sxs-lookup"><span data-stu-id="c75aa-115">*dwObjectID* is a dialog instance handle (either HDRVDIALOGINSTANCE or HTAPIDIALOGINSTANCE, depending on the context).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c75aa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c75aa-116">Requirements</span></span>



| <span data-ttu-id="c75aa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c75aa-117">Requirement</span></span> | <span data-ttu-id="c75aa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c75aa-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c75aa-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c75aa-119">TAPI version</span></span><br/> | <span data-ttu-id="c75aa-120">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c75aa-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c75aa-121">Header</span><span class="sxs-lookup"><span data-stu-id="c75aa-121">Header</span></span><br/>       | <dl> <span data-ttu-id="c75aa-122"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75aa-122"><dt>Tspi.h</dt></span></span> </dl> |



 

 




