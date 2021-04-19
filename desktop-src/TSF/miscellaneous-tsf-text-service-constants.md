---
title: Sonstige TSF-Text Dienst Konstanten (ctffunc. h)
description: Die folgenden Werte werden mit Text Diensten verwendet.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339579"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="5f741-103">Verschiedene TSF-Text Dienst Konstanten</span><span class="sxs-lookup"><span data-stu-id="5f741-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="5f741-104">Die folgenden Werte werden mit Text Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f741-104">The following values are used with text services.</span></span>



| <span data-ttu-id="5f741-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="5f741-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="5f741-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f741-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="5f741-107"><dt>**Tf \_ Menuready**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5f741-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="5f741-108">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f741-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="5f741-109"><dt>**Tf \_ Propui- \_ Status \_ savedefile**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5f741-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5f741-110">Die-Eigenschaft kann serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f741-110">The property can be serialized.</span></span> <span data-ttu-id="5f741-111">Wenn dieser Wert nicht vorhanden ist, kann die Eigenschaft nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f741-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="5f741-112">Dieser Wert wird mit [itffnpropertyuistatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) und [itffnpropertyuistatus:: SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f741-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5f741-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f741-113">Requirements</span></span>



| <span data-ttu-id="5f741-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f741-114">Requirement</span></span> | <span data-ttu-id="5f741-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f741-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f741-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f741-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f741-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f741-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f741-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f741-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f741-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f741-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5f741-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5f741-120">Redistributable</span></span><br/>          | <span data-ttu-id="5f741-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f741-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="5f741-122">Header</span><span class="sxs-lookup"><span data-stu-id="5f741-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f741-123"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f741-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f741-124">IDL</span><span class="sxs-lookup"><span data-stu-id="5f741-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f741-125"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f741-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f741-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f741-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f741-127">Itffnpropertyuistatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="5f741-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="5f741-128">Itffnpropertyuistatus:: SetStatus</span><span class="sxs-lookup"><span data-stu-id="5f741-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





