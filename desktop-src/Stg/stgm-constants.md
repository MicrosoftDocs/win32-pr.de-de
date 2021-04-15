---
title: STGM-Konstanten (objbase. h)
description: Flags, die Bedingungen für das Erstellen und Löschen des Objekts und der Zugriffs Modi für das Objekt angeben.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475480"
---
# <a name="stgm-constants"></a><span data-ttu-id="ed746-103">STGM-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ed746-103">STGM Constants</span></span>

<span data-ttu-id="ed746-104">Die STGM-Konstanten sind Flags, die die Bedingungen für das Erstellen und Löschen des Objekts und der Zugriffs Modi für das Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="ed746-105">Die STGM-Konstanten sind in den [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)-, [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)-und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstellen und in den Funktionen " [**stgforatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)", " [**stgfoatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)", "stgforatedocfileonilockbytes", " [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)" und " [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) " enthalten. [](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)</span><span class="sxs-lookup"><span data-stu-id="ed746-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="ed746-106">Diese Elemente werden häufig mit einem **or**-Operator kombiniert.</span><span class="sxs-lookup"><span data-stu-id="ed746-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="ed746-107">Sie werden in Gruppen wie in der folgenden Tabelle aufgeführt interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ed746-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="ed746-108">Es ist nicht zulässig, mehr als ein Element aus einer einzelnen Gruppe zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed746-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="ed746-109">Verwenden Sie ein Flag aus der Erstellungs Gruppe, wenn Sie ein Objekt erstellen, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="ed746-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="ed746-110">Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="ed746-111">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="ed746-111">Group</span></span>                      | <span data-ttu-id="ed746-112">Flag</span><span class="sxs-lookup"><span data-stu-id="ed746-112">Flag</span></span>                         | <span data-ttu-id="ed746-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ed746-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="ed746-114">Access</span><span class="sxs-lookup"><span data-stu-id="ed746-114">Access</span></span>                     | <span data-ttu-id="ed746-115">**STGM- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-115">**STGM\_READ**</span></span>               | <span data-ttu-id="ed746-116">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="ed746-117">**STGM- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="ed746-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="ed746-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="ed746-119">**STGM- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="ed746-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="ed746-120">0x00000002L</span></span> |
| <span data-ttu-id="ed746-121">Freigabe</span><span class="sxs-lookup"><span data-stu-id="ed746-121">Sharing</span></span>                    | <span data-ttu-id="ed746-122">**STGM- \_ Freigabe \_ Deny " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="ed746-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="ed746-123">0x00000040l</span><span class="sxs-lookup"><span data-stu-id="ed746-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="ed746-124">**STGM- \_ Freigabe \_ verweigern \_ Lesen**</span><span class="sxs-lookup"><span data-stu-id="ed746-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="ed746-125">0x00000030l</span><span class="sxs-lookup"><span data-stu-id="ed746-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="ed746-126">**STGM- \_ Freigabe \_ verweigern \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="ed746-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="ed746-127">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="ed746-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="ed746-128">**STGM- \_ Freigabe \_ exklusiv**</span><span class="sxs-lookup"><span data-stu-id="ed746-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="ed746-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="ed746-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="ed746-130">**STGM- \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="ed746-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="ed746-131">0x00040000l</span><span class="sxs-lookup"><span data-stu-id="ed746-131">0x00040000L</span></span> |
| <span data-ttu-id="ed746-132">Erstellung</span><span class="sxs-lookup"><span data-stu-id="ed746-132">Creation</span></span>                   | <span data-ttu-id="ed746-133">**STGM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="ed746-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="ed746-134">0x00001000l</span><span class="sxs-lookup"><span data-stu-id="ed746-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="ed746-135">**STGM \_ konvertieren**</span><span class="sxs-lookup"><span data-stu-id="ed746-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="ed746-136">0x00020000l</span><span class="sxs-lookup"><span data-stu-id="ed746-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="ed746-137">**STGM \_ FailIf**</span><span class="sxs-lookup"><span data-stu-id="ed746-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="ed746-138">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-138">0x00000000L</span></span> |
| <span data-ttu-id="ed746-139">Wird transakiert</span><span class="sxs-lookup"><span data-stu-id="ed746-139">Transactioning</span></span>             | <span data-ttu-id="ed746-140">**STGM \_ direkt**</span><span class="sxs-lookup"><span data-stu-id="ed746-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="ed746-141">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="ed746-142">**STGM \_ transaktiv**</span><span class="sxs-lookup"><span data-stu-id="ed746-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="ed746-143">0x00010000l</span><span class="sxs-lookup"><span data-stu-id="ed746-143">0x00010000L</span></span> |
| <span data-ttu-id="ed746-144">Transaktionsleistung</span><span class="sxs-lookup"><span data-stu-id="ed746-144">Transactioning Performance</span></span> | <span data-ttu-id="ed746-145">**STGM \_ noscratch**</span><span class="sxs-lookup"><span data-stu-id="ed746-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="ed746-146">0x00100000l</span><span class="sxs-lookup"><span data-stu-id="ed746-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="ed746-147">**STGM- \_ nosnapshot**</span><span class="sxs-lookup"><span data-stu-id="ed746-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="ed746-148">0x00200000l</span><span class="sxs-lookup"><span data-stu-id="ed746-148">0x00200000L</span></span> |
| <span data-ttu-id="ed746-149">Direkte austauschen und einfache</span><span class="sxs-lookup"><span data-stu-id="ed746-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="ed746-150">**STGM \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="ed746-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="ed746-151">0x08000000l</span><span class="sxs-lookup"><span data-stu-id="ed746-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="ed746-152">**STGM \_ Direct- \_ Austausch**</span><span class="sxs-lookup"><span data-stu-id="ed746-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="ed746-153">0x00400000l</span><span class="sxs-lookup"><span data-stu-id="ed746-153">0x00400000L</span></span> |
| <span data-ttu-id="ed746-154">Beim Release löschen</span><span class="sxs-lookup"><span data-stu-id="ed746-154">Delete On Release</span></span>          | <span data-ttu-id="ed746-155">**STGM \_ deleteonrelease**</span><span class="sxs-lookup"><span data-stu-id="ed746-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="ed746-156">0x04000000l</span><span class="sxs-lookup"><span data-stu-id="ed746-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="ed746-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-158">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-159">Gibt an, dass das Objekt schreibgeschützt ist, was bedeutet, dass keine Änderungen vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="ed746-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="ed746-160">Wenn z. b. ein Stream-Objekt mit **STGM- \_ Lese** Vorgang geöffnet wird, kann die [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) -Methode aufgerufen werden, die [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) -Methode jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="ed746-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="ed746-161">Ebenso kann, wenn ein Speicher Objekt, das mit **STGM- \_ Lese** Vorgang geöffnet wurde, die [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) -und [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) -Methode aufgerufen werden, aber die [**IStorage:: foatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -Methode und die [**IStorage:: foratestorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ed746-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM- \_ Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="ed746-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-164">Ermöglicht das Speichern von Änderungen am-Objekt, aber nicht den Zugriff auf seine Daten.</span><span class="sxs-lookup"><span data-stu-id="ed746-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="ed746-165">Der schreibgeschützte Modus wird von den bereitgestellten Implementierungen der [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle und der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed746-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM- \_ Lesevorgang**</span><span class="sxs-lookup"><span data-stu-id="ed746-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="ed746-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-168">Ermöglicht den Zugriff und die Änderung von Objektdaten.</span><span class="sxs-lookup"><span data-stu-id="ed746-168">Enables access and modification of object data.</span></span> <span data-ttu-id="ed746-169">Wenn z. b. ein Stream-Objekt in diesem Modus erstellt oder geöffnet wird, ist es möglich, sowohl [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) als auch **IStream:: Write** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed746-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="ed746-170">Beachten Sie, dass diese Konstante keine einfache Binärdatei **oder** Operation der Read-und **STGM- \_ Lese** Elemente von **STGM \_** ist.</span><span class="sxs-lookup"><span data-stu-id="ed746-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM- \_ Freigabe \_ Deny " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="ed746-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-172">0x00000040l</span><span class="sxs-lookup"><span data-stu-id="ed746-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-173">Gibt an, dass nachfolgende Öffnungen des Objekts keinen Lese-oder Schreibzugriff verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="ed746-174">Wenn kein Flag aus der Freigabe Gruppe angegeben wird, wird dieses Flag angenommen.</span><span class="sxs-lookup"><span data-stu-id="ed746-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM- \_ Freigabe \_ verweigern \_ Lesen**</span><span class="sxs-lookup"><span data-stu-id="ed746-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-176">0x00000030l</span><span class="sxs-lookup"><span data-stu-id="ed746-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-177">Verhindert, dass andere das Objekt später im **STGM- \_ Lesemodus** öffnen.</span><span class="sxs-lookup"><span data-stu-id="ed746-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="ed746-178">Sie wird in der Regel für ein Stamm Speicher Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed746-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM- \_ Freigabe \_ verweigern \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="ed746-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-180">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="ed746-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-181">Verhindert, dass andere das Objekt später für den Zugriff auf **STGM- \_ Schreib** -oder **STGM- \_ Lese** Vorgänge öffnen.</span><span class="sxs-lookup"><span data-stu-id="ed746-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="ed746-182">Im transaktiven Modus kann die Freigabe von " **STGM-Freigabe \_ \_ verweigern \_** " oder " **STGM \_ Freigabe \_ exklusiv** " die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ed746-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="ed746-183">Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM- \_ Freigabe \_ exklusiv**</span><span class="sxs-lookup"><span data-stu-id="ed746-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="ed746-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-186">Verhindert, dass andere das Objekt später in einem beliebigen Modus öffnen.</span><span class="sxs-lookup"><span data-stu-id="ed746-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="ed746-187">Beachten Sie, dass es sich bei diesem Wert nicht um eine einfache bitweise **or** -Operation der **STGM- \_ Freigabe \_ deny- \_ Lese** -und **STGM-Freigabe- \_ \_ \_ Schreib** Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="ed746-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="ed746-188">Im transaktiven Modus kann die Freigabe von " **STGM-Freigabe \_ \_ verweigern \_** " oder " **STGM \_ Freigabe \_ exklusiv** " die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ed746-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="ed746-189">Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM- \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="ed746-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-191">0x00040000l</span><span class="sxs-lookup"><span data-stu-id="ed746-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-192">Öffnet das Speicher Objekt mit exklusivem Zugriff auf die zuletzt zugesicherte Version.</span><span class="sxs-lookup"><span data-stu-id="ed746-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="ed746-193">Folglich können andere Benutzer keine Änderungen an dem Objekt übertragen, während Sie es im Prioritäts Modus geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="ed746-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="ed746-194">Sie profitieren von Leistungsvorteilen bei Kopier Vorgängen, aber Sie verhindern, dass andere Änderungen an Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ed746-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="ed746-195">Beschränken Sie den Zeitraum, in dem Objekte im Prioritäts Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="ed746-196">Sie müssen **STGM \_ Direct** und STGM mit dem Prioritäts Modus **\_ Lesen** angeben, und Sie können **STGM \_ deleteonrelease** nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="ed746-197">**STGM \_ Deleteonrelease** ist nur gültig, wenn ein Stamm Objekt erstellt wird, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="ed746-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="ed746-198">Dies ist nicht zulässig, wenn ein vorhandenes Stamm Objekt geöffnet wird, z. b. mit [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="ed746-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="ed746-199">Dies ist auch beim Erstellen oder Öffnen eines untergeordneten Elements (z. b. bei [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)) nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="ed746-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="ed746-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-201">0x00001000l</span><span class="sxs-lookup"><span data-stu-id="ed746-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-202">Gibt an, dass ein vorhandenes Speicher Objekt oder ein vorhandener Stream entfernt werden soll, bevor das neue Objekt es ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ed746-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="ed746-203">Ein neues-Objekt wird erstellt, wenn dieses Flag nur angegeben wird, wenn das vorhandene Objekt erfolgreich entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed746-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="ed746-204">Dieses Flag wird verwendet, wenn versucht wird, Folgendes zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="ed746-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="ed746-205">Ein Speicher Objekt auf einem Datenträger, aber eine Datei mit diesem Namen ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed746-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="ed746-206">Ein Objekt in einem Speicher Objekt, aber es ist ein Objekt mit dem angegebenen Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed746-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="ed746-207">Ein Bytearray-Objekt, aber eine mit dem angegebenen Namen ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed746-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="ed746-208">Dieses Flag kann nicht mit offenen Vorgängen verwendet werden, wie z. b. [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) oder [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="ed746-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ konvertieren**</span><span class="sxs-lookup"><span data-stu-id="ed746-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-210">0x00020000l</span><span class="sxs-lookup"><span data-stu-id="ed746-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-211">Erstellt das neue-Objekt, während vorhandene Daten in einem Stream mit dem Namen "Content" beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="ed746-212">Bei einem Speicher Objekt oder einem Bytearray werden die alten Daten in einen Stream formatiert, unabhängig davon, ob die vorhandene Datei oder das Bytearray derzeit ein mehrschichtiges Speicher Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="ed746-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="ed746-213">Dieses Flag kann nur beim Erstellen eines Stamm Speicher Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="ed746-214">Sie kann nicht innerhalb eines Speicher Objekts verwendet werden. beispielsweise in [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="ed746-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="ed746-215">Es ist auch ungültig, dieses Flag und das **STGM \_ deleteonrelease** -Flag gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed746-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FailIf**</span><span class="sxs-lookup"><span data-stu-id="ed746-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-217">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-218">Bewirkt, dass der Erstellungs Vorgang fehlschlägt, wenn ein vorhandenes Objekt mit dem angegebenen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ed746-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="ed746-219">In diesem Fall wird **STG \_ E \_ filealleseryist** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="ed746-220">Dies ist der Standard Erstellungs Modus. Das heißt, wenn kein anderes Create-Flag angegeben ist, wird **STGM \_ failisthere** impliziert.</span><span class="sxs-lookup"><span data-stu-id="ed746-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ direkt**</span><span class="sxs-lookup"><span data-stu-id="ed746-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-222">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="ed746-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-223">Gibt an, dass im direkten Modus jede Änderung an einem Speicher-oder streamelement geschrieben wird, wenn es auftritt.</span><span class="sxs-lookup"><span data-stu-id="ed746-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="ed746-224">Dies ist die Standardeinstellung, wenn weder **STGM \_ Direct** noch **STGM \_ transaktiv** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transaktiv**</span><span class="sxs-lookup"><span data-stu-id="ed746-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-226">0x00010000l</span><span class="sxs-lookup"><span data-stu-id="ed746-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-227">Gibt an, dass Änderungen im transaktiven Modus nur gepuffert und geschrieben werden, wenn ein expliziter Commit-Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="ed746-228">Um die Änderungen zu ignorieren, müssen Sie die [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) -Methode in der [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)-, [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)-oder [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed746-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="ed746-229">Die Implementierung der com-Verbund Datei von **IStorage** unterstützt keine transaktiven Streams. Dies bedeutet, dass Datenströme nur im direkten Modus geöffnet werden können, und Sie können keine Änderungen an diesen Datenströmen zurücksetzen. transaktive Speicher werden jedoch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed746-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="ed746-230">Die Verbund Datei-, eigenständige und NTFS-Dateisystem Implementierungen von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützen auf ähnliche Weise keine transaktiven, einfachen Eigenschaften Sätze, da diese Eigenschaften Sätze in Datenströmen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="ed746-231">Das transaktionsset von nicht einfachen Eigenschafts Sätzen, das durch Angeben des **\_ nicht einfache-Flags propsetflag** im *grfFlags* -Parameter von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)erstellt werden kann, wird jedoch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed746-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ noscratch**</span><span class="sxs-lookup"><span data-stu-id="ed746-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-233">0x00100000l</span><span class="sxs-lookup"><span data-stu-id="ed746-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-234">Gibt an, dass im transaktiven Modus normalerweise eine temporäre Scratch-Datei verwendet wird, um Änderungen zu speichern, bis die **Commit** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="ed746-235">Wenn Sie **STGM \_ noscratch** angeben, können Sie den nicht verwendeten Teil der ursprünglichen Datei als Arbeitsbereich verwenden, anstatt für diesen Zweck eine neue Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed746-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="ed746-236">Dies wirkt sich nicht auf die Daten in der ursprünglichen Datei aus, und in bestimmten Fällen kann die Leistung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="ed746-237">Es ist nicht zulässig, dieses Flag anzugeben, ohne auch **STGM \_ transaktiv** anzugeben, und dieses Flag kann nur in einem geöffneten Stamm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="ed746-238">Weitere Informationen zum noscratch-Modus finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM- \_ nosnapshot**</span><span class="sxs-lookup"><span data-stu-id="ed746-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-240">0x00200000l</span><span class="sxs-lookup"><span data-stu-id="ed746-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-241">Dieses Flag wird verwendet, wenn ein Speicher Objekt mit **STGM \_ transaktiv** und ohne **STGM- \_ Freigabe \_ exklusiv** oder **STGM- \_ Freigabe deny- \_ \_ Schreibvorgang** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="ed746-242">In diesem Fall verhindert die Angabe von **STGM \_ nosnapshot** , dass die vom System bereitgestellte Implementierung eine Momentaufnahme Kopie der Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed746-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="ed746-243">Stattdessen werden Änderungen an der Datei an das Ende der Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed746-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="ed746-244">Nicht verwendeter Speicherplatz wird erst freigegeben, wenn die Konsolidierung während des Commit durchgeführt wird und nur ein aktueller Writer für die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ed746-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="ed746-245">Wenn die Datei im Modus keine Momentaufnahme geöffnet ist, kann kein anderer Öffnungsvorgang durchgeführt werden, ohne **STGM \_ nosnapshot** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="ed746-246">Dieses Flag kann nur in einem Stamm Öffnungsvorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="ed746-247">Weitere Informationen zum nosnapshot-Modus finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="ed746-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-249">0x08000000l</span><span class="sxs-lookup"><span data-stu-id="ed746-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-250">Bietet eine schnellere Implementierung einer Verbund Datei in einer begrenzten, aber häufig verwendeten Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="ed746-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="ed746-251">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ Direct- \_ Austausch**</span><span class="sxs-lookup"><span data-stu-id="ed746-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-253">0x00400000l</span><span class="sxs-lookup"><span data-stu-id="ed746-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-254">Unterstützt den direkten Modus für Datei Vorgänge mit einem einzelnen Writer und mehreren Lesevorgängen.</span><span class="sxs-lookup"><span data-stu-id="ed746-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="ed746-255">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed746-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed746-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ deleteonrelease**</span><span class="sxs-lookup"><span data-stu-id="ed746-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed746-257">0x04000000l</span><span class="sxs-lookup"><span data-stu-id="ed746-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="ed746-258">Gibt an, dass die zugrunde liegende Datei automatisch zerstört werden soll, wenn das Stamm Speicher Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="ed746-259">Diese Funktion ist besonders nützlich für das Erstellen temporärer Dateien.</span><span class="sxs-lookup"><span data-stu-id="ed746-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="ed746-260">Dieses Flag kann nur verwendet werden, wenn ein Stamm Objekt erstellt wird, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="ed746-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="ed746-261">Dies ist nicht zulässig, wenn ein Stamm Objekt geöffnet wird, z. b. mit [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), oder wenn ein Unterelement erstellt oder geöffnet wird, z. b. mit [**IStorage:: foatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="ed746-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="ed746-262">Es ist auch nicht zulässig, dieses Flag und das STGM- \_ Convert-Flag gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed746-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed746-263">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed746-263">Remarks</span></span>

<span data-ttu-id="ed746-264">Sie können diese Flags kombinieren, aber Sie können nur ein Flag aus jeder Gruppe verwandter Flags auswählen.</span><span class="sxs-lookup"><span data-stu-id="ed746-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="ed746-265">In der Regel muss für alle Funktionen und Methoden, die diese Konstanten verwenden, ein Flag aus den einzelnen Zugriffs-und Freigabe Gruppen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="ed746-266">Flags aus anderen Gruppen sind optional.</span><span class="sxs-lookup"><span data-stu-id="ed746-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="ed746-267">Transaktiver Modus</span><span class="sxs-lookup"><span data-stu-id="ed746-267">Transacted Mode</span></span>

<span data-ttu-id="ed746-268">Wenn das " **STGM \_ Direct**"-Flag angegeben ist, kann nur eine der folgenden Kombinationen von Flags aus den Zugriffs-und Freigabe Gruppen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="ed746-269">Beachten Sie, dass der direkte Modus durch das Fehlen von **STGM- \_ Transaktionen** impliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="ed746-270">Das heißt, wenn weder " **STGM \_ Direct** " noch " **STGM \_ transagiert** " angegeben wird, wird **STGM \_ Direct** angenommen.</span><span class="sxs-lookup"><span data-stu-id="ed746-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="ed746-271">Wenn das **\_ transaktive STGM** -Flag angegeben wird, werden Objekte im transaktiven Modus erstellt oder geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ed746-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="ed746-272">In diesem Modus werden Änderungen an einem Objekt erst beibehalten, wenn ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="ed746-273">Beispielsweise werden Änderungen an einem transaktiven Speicher Objekt nicht persistent gespeichert, bis die [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="ed746-274">Änderungen an einem solchen Speicher Objekt gehen verloren, wenn das Speicher Objekt freigegeben wird (endgültige Version), bevor die **Commit** -Methode aufgerufen wird, oder wenn die [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="ed746-275">Wenn ein Objekt im transaktiven Modus erstellt oder geöffnet wird, muss die Implementierung sowohl die ursprünglichen Daten als auch die Updates für diese Daten beibehalten, damit Updates bei Bedarf wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="ed746-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="ed746-276">Dies erfolgt in der Regel durch das Schreiben von Änderungen in einen Grundbereich, bis ein Commit ausgeführt wird, oder durch Erstellen einer Kopie, die als Momentaufnahme bezeichnet wird, der zuletzt ausgeführten Daten.</span><span class="sxs-lookup"><span data-stu-id="ed746-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="ed746-277">Wenn ein Stamm Speicher Objekt im transaktiven Modus geöffnet wird, können der Speicherort und das Verhalten der Rohdaten und der Momentaufnahme Kopien gesteuert werden, um die Leistung mit den nosnapshot-Flags " **STGM \_ noscratch** " und " **STGM \_ nosnapshot** " zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="ed746-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="ed746-278">(Ein Stamm Speicher Objekt wird z. b. aus der [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) -Funktion abgerufen; ein Speicher Objekt, das von der [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) -Methode abgerufen wurde, ist ein unter Speicher Objekt.) Normalerweise werden die Daten und Momentaufnahmen der Daten in temporären Dateien gespeichert, die vom Speicher getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="ed746-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="ed746-279">Die Auswirkung dieser Flags hängt von der Anzahl der Leser und/oder Writer ab, die auf den Stamm Speicher zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ed746-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="ed746-280">Im "Single-Writer"-Fall wird ein Speicher Objekt im Transaktionsmodus für den Schreibzugriff geöffnet, und es kann kein anderer Zugriff auf die Datei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ed746-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="ed746-281">Das heißt, die Datei wird mit **STGM \_ transaktiv** geöffnet, Zugriff auf **STGM- \_ Schreib** -oder **STGM- \_ Lese** Vorgänge und die Freigabe der **STGM- \_ Freigabe \_ exklusiv**.</span><span class="sxs-lookup"><span data-stu-id="ed746-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="ed746-282">In diesem Fall werden Änderungen am Speicher Objekt in den Scratch-Bereich geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed746-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="ed746-283">Wenn für diese Änderungen ein Commit ausgeführt wird, werden Sie in den ursprünglichen Speicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="ed746-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="ed746-284">Wenn keine Änderungen am Speicher Objekt tatsächlich vorgenommen werden, werden daher keine unnötigen Datenübertragungen übertragen.</span><span class="sxs-lookup"><span data-stu-id="ed746-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="ed746-285">Im Fall von "Multiple-Writer" wird ein transaktives Speicher Objekt für den Schreibzugriff geöffnet, aber es wird in derartigen Form verwendet, um andere Writer zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="ed746-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="ed746-286">Das heißt, dass das Speicher Objekt mit **STGM \_ transaktiv** geöffnet wird, Zugriff auf **STGM- \_ Schreib** Vorgänge oder STGM-Lesevorgänge hat und die Freigabe von STGM-Freigaben **\_ \_ verweigern \_ gelesen** wird. **\_**</span><span class="sxs-lookup"><span data-stu-id="ed746-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="ed746-287">Wenn stattdessen die Freigabe von **STGM- \_ Freigabe \_ deny \_** nicht angegeben wird, ist der Fall "Multiple-Writer, Multiple-Reader".</span><span class="sxs-lookup"><span data-stu-id="ed746-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="ed746-288">In diesen Fällen wird während des Öffnungs Vorgangs eine Momentaufnahme der ursprünglichen Daten erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed746-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="ed746-289">Daher ist auch dann, wenn keine Änderungen am Speicher vorgenommen werden und/oder wenn er nicht gleichzeitig von einem anderen Writer geöffnet wird, die Datenübertragung während des Öffnens erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed746-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="ed746-290">Demzufolge kann die beste Leistung bei der Leistung erreicht werden, indem das Speicher Objekt in der **STGM- \_ Freigabe \_ deny- \_ Schreib** -oder **STGM- \_ Freigabe \_ exklusiver** Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="ed746-291">Weitere Informationen darüber, wie für Änderungen ein Commit ausgeführt wird, wenn mehrere Writer vorhanden sind, finden Sie unter [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="ed746-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="ed746-292">Im Fall von "Single-Writer, Multiple-Reader" wird ein transaktives Speicher Objekt für den Schreibzugriff geöffnet, aber für Leser freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="ed746-293">Das heißt, das Speicher Objekt wird vom Writer mit **STGM- \_ Transaktionen**, den Zugriff auf **STGM- \_ Lese** -oder **STGM- \_ Schreib** Vorgänge und die Freigabe von STGM-Freigaben zum **Verweigern von \_ \_ \_ Schreib** Zugriff geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ed746-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="ed746-294">Der Speicher wird von Lesern mit **gegm- \_ transaktive**, dem Zugriff auf **STGM- \_ Lese** Vorgänge und der Freigabe der **STGM- \_ Freigabe \_ deny \_ None** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ed746-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="ed746-295">In diesem Fall verwendet der Writer den Bereich Scratch zum Speichern von Änderungen, für die kein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed746-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="ed746-296">Wie in den obigen Fällen gibt es bei dem Reader eine Öffnungszeit-Leistungs Einbuße, während eine Momentaufnahme Kopie der Daten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="ed746-297">In der Regel ist der Grundbereich eine temporäre Datei, getrennt von den ursprünglichen Daten.</span><span class="sxs-lookup"><span data-stu-id="ed746-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="ed746-298">Wenn Änderungen an der ursprünglichen Datei vorgenommen werden, müssen die Daten aus der temporären Datei übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="ed746-299">Um diese Datenübertragung zu vermeiden, kann das Flag " **STGM \_ noscratch**" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="ed746-300">Wenn dieses Flag angegeben wird, werden Teile der Speicher Objektdatei für den Bereich Scratch anstelle einer separaten temporären Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed746-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="ed746-301">Folglich kann das Ausführen eines Commits für Änderungen schnell erfolgen, da nur wenige Datenübertragungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ed746-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="ed746-302">Der Nachteil ist, dass die Speicherdatei größer werden kann, als Sie andernfalls wäre, da Sie für die ursprünglichen Daten und den Grundbereich groß genug vergrößert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ed746-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="ed746-303">Um die Daten zu konsolidieren und diesen unnötigen Bereich zu entfernen, öffnen Sie den Stamm Speicher im transaktiven Modus erneut, ohne das Flag " **STGM \_ noscratch** " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ed746-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="ed746-304">Nennen Sie dann [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) , wobei das **stgc- \_ konsoliderflag** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ed746-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="ed746-305">Der momentaufnahmenbereich ist wie der Scratch-Bereich auch eine temporäre Datei. Dies kann auch mit einem STGM-Flag beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="ed746-306">Wenn das Flag " **STGM \_ nosnapshot** " angegeben wird, wird keine separate temporäre Momentaufnahme Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed746-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="ed746-307">Stattdessen werden die ursprünglichen Daten nie geändert, auch wenn mindestens ein Writer pro Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ed746-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="ed746-308">Wenn für Änderungen ein Commit ausgeführt wird, werden Sie der Datei hinzugefügt, die ursprünglichen Daten bleiben jedoch intakt.</span><span class="sxs-lookup"><span data-stu-id="ed746-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="ed746-309">Durch diesen Modus wird die Effizienz gesteigert, da die Laufzeit dadurch reduziert wird, dass während des Öffnungs Vorgangs keine Momentaufnahme erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ed746-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="ed746-310">Wenn Sie diesen Modus verwenden, kann es jedoch zu einer sehr großen Speicherdatei kommen, da die Daten in der Datei nie überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="ed746-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="ed746-311">Dies gilt nicht für die Größe der Dateien, die im nosnapshot-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="ed746-312">Direkter Single-Writer, Multiple-Reader Modus</span><span class="sxs-lookup"><span data-stu-id="ed746-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="ed746-313">Wie bereits beschrieben, ist es möglich, einen einzelnen Writer und mehrere Leser eines Speicher Objekts zu haben, wenn dieses Objekt im transaktiven Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="ed746-314">Es ist auch möglich, den Single Writer-multireader-Fall im direkten Modus zu erreichen, indem Sie das " **STGM \_ Direct \_ allemr** "-Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="ed746-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="ed746-315">In **STGM \_ Direct- \_ taumr** -Modus ist es möglich, dass ein Aufrufer ein Objekt für den Lese-/Schreibzugriff öffnet, während andere Aufrufer gleichzeitig die Datei für den schreibgeschützten Zugriff geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="ed746-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="ed746-316">Es ist nicht zulässig, dieses Flag in Kombination mit dem per **STGM \_ transaktiven** Flag zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed746-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="ed746-317">In diesem Modus öffnet der Writer das-Objekt mit den folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="ed746-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="ed746-318">**STGM \_ direkter \_ Austausch** von "STGM", "STGM"- \| **\_** \| **\_ Freigabe " \_ denywrite** "</span><span class="sxs-lookup"><span data-stu-id="ed746-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="ed746-319">und jeder Leser öffnet das Objekt mit den folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="ed746-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="ed746-320">**STGM \_ direkter \_ Austausch** von "STGM" \| **\_ Lesen** \| **STGM- \_ Freigabe \_ verweigern \_**</span><span class="sxs-lookup"><span data-stu-id="ed746-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="ed746-321">In diesem Modus muss der Writer exklusiven Zugriff auf das Objekt erhalten, um das Speicher Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ed746-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="ed746-322">Dies ist möglich, wenn Sie von allen Lesern geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="ed746-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="ed746-323">Der Writer verwendet die [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) -Schnittstelle, um diesen exklusiven Zugriff zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ed746-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="ed746-324">Einfacher Modus</span><span class="sxs-lookup"><span data-stu-id="ed746-324">Simple Mode</span></span>

<span data-ttu-id="ed746-325">Der einfache Modus (**STGM \_ Simple**) ist für Anwendungen nützlich, die vollständige Speichervorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed746-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="ed746-326">Es ist zwar effizient, weist jedoch die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="ed746-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="ed746-327">Für substorages ist keine Unterstützung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed746-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="ed746-328">Das Speicher Objekt und die Streamobjekte, die daraus abgerufen werden, können nicht gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="ed746-329">Jeder Stream weist eine minimale Größe auf.</span><span class="sxs-lookup"><span data-stu-id="ed746-329">Each stream has a minimum size.</span></span> <span data-ttu-id="ed746-330">Wenn beim Freigeben des Streams weniger als die minimalen Bytes in einen Stream geschrieben werden, wird der Datenstrom auf die minimale Größe erweitert.</span><span class="sxs-lookup"><span data-stu-id="ed746-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="ed746-331">Die Mindestgröße für eine bestimmte [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Implementierung beträgt z. b. 4 KB.</span><span class="sxs-lookup"><span data-stu-id="ed746-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="ed746-332">Es wird ein Stream erstellt und 1 KB darin geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed746-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="ed746-333">Bei der endgültigen Version dieses **IStream** wird die Streamgröße automatisch auf 4 KB erweitert.</span><span class="sxs-lookup"><span data-stu-id="ed746-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="ed746-334">Wenn Sie anschließend den Stream öffnen und die [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode aufrufen, wird eine Größe von 4 KB angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed746-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="ed746-335">Nicht alle Methoden von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) werden von der Implementierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed746-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="ed746-336">Weitere Informationen finden Sie unter [IStorage-Verbund Datei Implementierung](istorage-compound-file-implementation.md)und [Implementierung der IStream-Verbund Datei](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ed746-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="ed746-337">Das Marshalling [ist das](/windows/desktop/Midl/marshaling-ole-data-types) Verpacken, entpacken und Senden von Schnittstellen Methoden Parametern über Thread-oder Prozess Grenzen hinweg innerhalb eines Remote Prozedur Aufrufs (RPC).</span><span class="sxs-lookup"><span data-stu-id="ed746-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="ed746-338">Weitere Informationen finden Sie unter Marshalling von [Details](../com/marshaling-details.md) und [Schnittstellen](../com/interface-marshaling.md)Marshalling.</span><span class="sxs-lookup"><span data-stu-id="ed746-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="ed746-339">Wenn ein Speicher Objekt von einem Create-Vorgang im einfachen Modus abgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="ed746-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="ed746-340">Streamelemente können erstellt, aber nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed746-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="ed746-341">Wenn ein Stream-Element durch Aufrufen von [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)erstellt wird, ist es nicht möglich, einen weiteren Stream zu erstellen, bis das Stream-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed746-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="ed746-342">Nachdem alle Streams geschrieben wurden, wird [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) aufgerufen, um die Änderungen zu leeren.</span><span class="sxs-lookup"><span data-stu-id="ed746-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="ed746-343">Wenn ein Speicher Objekt von einem Öffnungsvorgang im einfachen Modus abgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="ed746-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="ed746-344">Es ist möglich, jeweils nur ein streamelement zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ed746-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="ed746-345">Es ist nicht möglich, die Größe eines Streams zu ändern, indem Sie die [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) -Methode aufrufen oder über das Ende des Streams hinaus suchen oder schreiben.</span><span class="sxs-lookup"><span data-stu-id="ed746-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="ed746-346">Da allerdings alle Streams eine minimale Größe haben, ist es möglich, den Stream bis zu dieser Größe zu verwenden, auch wenn weniger Daten ursprünglich in den Datenstrom geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="ed746-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="ed746-347">Verwenden Sie die [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode, um die Größe eines Streams zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ed746-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="ed746-348">Wenn ein Speicher Element von einem Speicher Objekt geändert wird, das sich nicht im einfachen Modus befindet, ist es nicht mehr möglich, dieses Speicher Element im einfachen Modus zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ed746-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed746-349">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed746-349">Requirements</span></span>



| <span data-ttu-id="ed746-350">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed746-350">Requirement</span></span> | <span data-ttu-id="ed746-351">Wert</span><span class="sxs-lookup"><span data-stu-id="ed746-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed746-352">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed746-352">Minimum supported client</span></span><br/> | <span data-ttu-id="ed746-353">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed746-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ed746-354">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed746-354">Minimum supported server</span></span><br/> | <span data-ttu-id="ed746-355">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed746-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed746-356">Header</span><span class="sxs-lookup"><span data-stu-id="ed746-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed746-357"><dt>Objbase. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed746-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed746-358">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed746-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed746-359">**ISequentialStream:: Read**</span><span class="sxs-lookup"><span data-stu-id="ed746-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="ed746-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="ed746-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="ed746-361">**Stgkreatedocfile**</span><span class="sxs-lookup"><span data-stu-id="ed746-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="ed746-362">**Stgkreatedocfileonilockbytes**</span><span class="sxs-lookup"><span data-stu-id="ed746-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="ed746-363">**Stgkreatestorageex**</span><span class="sxs-lookup"><span data-stu-id="ed746-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="ed746-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="ed746-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="ed746-365">**Stgopenstorageex**</span><span class="sxs-lookup"><span data-stu-id="ed746-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="ed746-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="ed746-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

