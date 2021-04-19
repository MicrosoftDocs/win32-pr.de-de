---
title: Functions (STG)
description: Funktionen sind Routinen oder Unterroutinen, die einen bestimmten Wert oder Werte zurückgeben. Strukturierte Speicherfunktionen werden in den folgenden Abschnitten beschrieben.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Strukturierter Speicher, Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106360459"
---
# <a name="structured-storage-functions"></a><span data-ttu-id="c37f4-105">Strukturierte Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="c37f4-105">Structured Storage functions</span></span>

<span data-ttu-id="c37f4-106">Funktionen sind Routinen oder Unterroutinen, die einen bestimmten Wert oder Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c37f4-106">Functions are routines or subroutines that return a specific value or values.</span></span> <span data-ttu-id="c37f4-107">Strukturierte Speicherfunktionen werden in den folgenden Abschnitten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c37f4-107">Structured Storage functions are described in the following sections:</span></span>

-   [<span data-ttu-id="c37f4-108">**"Kreateilockbytesonhglobal"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-108">**CreateILockBytesOnHGlobal**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [<span data-ttu-id="c37f4-109">**"Kreatestreamonhglobal"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-109">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [<span data-ttu-id="c37f4-110">**Fmtidtopropstgname**</span><span class="sxs-lookup"><span data-stu-id="c37f4-110">**FmtIdToPropStgName**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [<span data-ttu-id="c37f4-111">**"Frepropvariantarray"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-111">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="c37f4-112">**Getconvertstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-112">**GetConvertStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [<span data-ttu-id="c37f4-113">**GetHGlobalFromILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-113">**GetHGlobalFromILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [<span data-ttu-id="c37f4-114">**Gethglobalfromstream**</span><span class="sxs-lookup"><span data-stu-id="c37f4-114">**GetHGlobalFromStream**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [<span data-ttu-id="c37f4-115">**Oleconvertistoragetoolestream**</span><span class="sxs-lookup"><span data-stu-id="c37f4-115">**OleConvertIStorageToOLESTREAM**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [<span data-ttu-id="c37f4-116">**Oleconvertistoragetoolestreamex**</span><span class="sxs-lookup"><span data-stu-id="c37f4-116">**OleConvertIStorageToOLESTREAMEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [<span data-ttu-id="c37f4-117">**Oleconvertolestreamtoistorage**</span><span class="sxs-lookup"><span data-stu-id="c37f4-117">**OleConvertOLESTREAMToIStorage**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [<span data-ttu-id="c37f4-118">**Oleconvertolestreamtoistorageex**</span><span class="sxs-lookup"><span data-stu-id="c37f4-118">**OleConvertOLESTREAMToIStorageEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [<span data-ttu-id="c37f4-119">**Propstgnametofmtid**</span><span class="sxs-lookup"><span data-stu-id="c37f4-119">**PropStgNameToFmtId**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [<span data-ttu-id="c37f4-120">**Propvariantclear**</span><span class="sxs-lookup"><span data-stu-id="c37f4-120">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="c37f4-121">**Propvariantcopy**</span><span class="sxs-lookup"><span data-stu-id="c37f4-121">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [<span data-ttu-id="c37f4-122">**Propvariantinit**</span><span class="sxs-lookup"><span data-stu-id="c37f4-122">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="c37f4-123">**"Read classstg"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-123">**ReadClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [<span data-ttu-id="c37f4-124">**Read classstm**</span><span class="sxs-lookup"><span data-stu-id="c37f4-124">**ReadClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [<span data-ttu-id="c37f4-125">**"Read fmtusertypestg"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-125">**ReadFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [<span data-ttu-id="c37f4-126">**Stgconvertpropertyumvariant**</span><span class="sxs-lookup"><span data-stu-id="c37f4-126">**StgConvertPropertyToVariant**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [<span data-ttu-id="c37f4-127">**Setconvertstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-127">**SetConvertStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [<span data-ttu-id="c37f4-128">**Stgconvertvarianttoproperty**</span><span class="sxs-lookup"><span data-stu-id="c37f4-128">**StgConvertVariantToProperty**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [<span data-ttu-id="c37f4-129">**Stgkreatedocfile**</span><span class="sxs-lookup"><span data-stu-id="c37f4-129">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [<span data-ttu-id="c37f4-130">**Stgkreatedocfileonilockbytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-130">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [<span data-ttu-id="c37f4-131">**Stgkreatepropsetstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-131">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [<span data-ttu-id="c37f4-132">**Stgkreatepropstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-132">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [<span data-ttu-id="c37f4-133">**Stgkreatestorageex**</span><span class="sxs-lookup"><span data-stu-id="c37f4-133">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [<span data-ttu-id="c37f4-134">**Stgdeserializepropvariant**</span><span class="sxs-lookup"><span data-stu-id="c37f4-134">**StgDeserializePropVariant**</span></span>](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [<span data-ttu-id="c37f4-135">**Stggetifilllockbytesonfile**</span><span class="sxs-lookup"><span data-stu-id="c37f4-135">**StgGetIFillLockBytesOnFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [<span data-ttu-id="c37f4-136">**Stggetifilllockbytesonilockbytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-136">**StgGetIFillLockBytesOnILockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [<span data-ttu-id="c37f4-137">**Stgisstoragefile**</span><span class="sxs-lookup"><span data-stu-id="c37f4-137">**StgIsStorageFile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [<span data-ttu-id="c37f4-138">**StgIsStorageILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-138">**StgIsStorageILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [<span data-ttu-id="c37f4-139">**Stgopenasyncdocfileonifilllockbytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [<span data-ttu-id="c37f4-140">**Stgopenlayoutdocfile**</span><span class="sxs-lookup"><span data-stu-id="c37f4-140">**StgOpenLayoutDocfile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [<span data-ttu-id="c37f4-141">**Stgopenpropstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-141">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [<span data-ttu-id="c37f4-142">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="c37f4-142">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [<span data-ttu-id="c37f4-143">**Stgopenstorageex**</span><span class="sxs-lookup"><span data-stu-id="c37f4-143">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [<span data-ttu-id="c37f4-144">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-144">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [<span data-ttu-id="c37f4-145">**Stgpropertylengthasvariant**</span><span class="sxs-lookup"><span data-stu-id="c37f4-145">**StgPropertyLengthAsVariant**</span></span>](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [<span data-ttu-id="c37f4-146">**Stgserializepropvariant**</span><span class="sxs-lookup"><span data-stu-id="c37f4-146">**StgSerializePropVariant**</span></span>](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [<span data-ttu-id="c37f4-147">**Stgsettimes**</span><span class="sxs-lookup"><span data-stu-id="c37f4-147">**StgSetTimes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [<span data-ttu-id="c37f4-148">**Schreibclassstg**</span><span class="sxs-lookup"><span data-stu-id="c37f4-148">**WriteClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [<span data-ttu-id="c37f4-149">**Schreib classstm**</span><span class="sxs-lookup"><span data-stu-id="c37f4-149">**WriteClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [<span data-ttu-id="c37f4-150">**"Schreibfmtusertypestg"**</span><span class="sxs-lookup"><span data-stu-id="c37f4-150">**WriteFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
