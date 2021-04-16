---
description: 'Weitere Informationen finden Sie unter: esentobsoleteexception-Klasse'
title: EsentObsoleteException-Klasse
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530437"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="0a53a-103">EsentObsoleteException-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a53a-103">EsentObsoleteException class</span></span>

<span data-ttu-id="0a53a-104">Basisklasse für veraltete Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="0a53a-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0a53a-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="0a53a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0a53a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a53a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0a53a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0a53a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0a53a-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0a53a-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0a53a-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="0a53a-111">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="0a53a-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a53a-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a53a-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0a53a-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a53a-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a53a-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="0a53a-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="0a53a-115">Thread safety</span></span>

<span data-ttu-id="0a53a-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="0a53a-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0a53a-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="0a53a-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a53a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a53a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a53a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="0a53a-119">Reference</span></span>

[<span data-ttu-id="0a53a-120">Esentobsoleteexception-Member</span><span class="sxs-lookup"><span data-stu-id="0a53a-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="0a53a-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0a53a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="0a53a-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="0a53a-122">Derived types</span></span>

[<span data-ttu-id="0a53a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a53a-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0a53a-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0a53a-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0a53a-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0a53a-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0a53a-127">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="0a53a-128">Microsoft. ISAM. ESENT. Interop. esentobsoleteexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="0a53a-129">Microsoft. ISAM. ESENT. Interop. esentaccessdeniedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="0a53a-130">Microsoft. ISAM. ESENT. Interop. esentbadbackupdatabasesizeexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="0a53a-131">Microsoft. ISAM. ESENT. Interop. esentbadbookmarkexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="0a53a-132">Microsoft. ISAM. ESENT. Interop. esentbaddbsignatureexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="0a53a-133">Microsoft. ISAM. ESENT. Interop. esentbadpatchpageexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="0a53a-134">Microsoft. ISAM. ESENT. Interop. esentbadslvsignatureexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="0a53a-135">Microsoft. ISAM. ESENT. Interop. esentcannotaddfixedvarcolumninderivedtableexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="0a53a-136">Microsoft. ISAM. ESENT. Interop. esentcannotnestdistributedtransaktionsexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="0a53a-137">Microsoft. ISAM. ESENT. Interop. esentcolumnindexedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="0a53a-138">Microsoft. ISAM. ESENT. Interop. esentcolumninrelationshipexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="0a53a-139">Microsoft. ISAM. ESENT. Interop. esentcolumnlongexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="0a53a-140">Microsoft. ISAM. ESENT. Interop. esentcontainernotemptyexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="0a53a-141">Microsoft. ISAM. ESENT. Interop. esentchangecystackouesf memoryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="0a53a-142">Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="0a53a-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="0a53a-143">Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException</span><span class="sxs-lookup"><span data-stu-id="0a53a-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="0a53a-144">Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException</span><span class="sxs-lookup"><span data-stu-id="0a53a-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="0a53a-145">Microsoft. ISAM. ESENT. Interop. esentdatabaseidinuseexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="0a53a-146">Microsoft. ISAM. ESENT. Interop. esentdatabasepatchfilemismatchexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="0a53a-147">Microsoft. ISAM. ESENT. Interop. esentdatabasesnotfromsamesnapshotexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="0a53a-148">Microsoft. ISAM. ESENT. Interop. esentdatabasestreamingfilemismatchexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="0a53a-149">Microsoft. ISAM. ESENT. Interop. esentdatabaseunavailableexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="0a53a-150">Microsoft. ISAM. ESENT. Interop. esentdatahaschangedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="0a53a-151">Microsoft. ISAM. ESENT. Interop. esentdistributedtransaktionalleserypreparedumcommitexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="0a53a-152">Microsoft. ISAM. ESENT. Interop. esentdistributedtransaktionnotyetprepareddecommitexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="0a53a-153">Microsoft. ISAM. ESENT. Interop. esentdtccallbackunexpectederrorexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="0a53a-154">Microsoft. ISAM. ESENT. Interop. esentdtcmissingcallbackexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="0a53a-155">Microsoft. ISAM. ESENT. Interop. esentdtcmissingcallbackonherstellyexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="0a53a-156">Microsoft. ISAM. ESENT. Interop. esentfilecloseexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="0a53a-157">Microsoft. ISAM. ESENT. Interop. esentfileioabortexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="0a53a-158">Microsoft. ISAM. ESENT. Interop. esentfileiofailexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="0a53a-159">Microsoft. ISAM. ESENT. Interop. esentfileioretryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="0a53a-160">Microsoft. ISAM. ESENT. Interop. esentfileiosparseexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="0a53a-161">Microsoft. ISAM. ESENT. Interop. esentindexcantbuildexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="0a53a-162">Microsoft. ISAM. ESENT. Interop. esentindextuplestoomanycolumnsexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="0a53a-163">Microsoft. ISAM. ESENT. Interop. esentinvalidcountryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="0a53a-164">Microsoft. ISAM. ESENT. Interop. esentinvaliddateinameexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="0a53a-165">Microsoft. ISAM. ESENT. Interop. esentinvalidlogdirectoriyexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="0a53a-166">Microsoft. ISAM. ESENT. Interop. esentinvalidloggedoperationexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="0a53a-167">Microsoft. ISAM. ESENT. Interop. esentinvalidobjectexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="0a53a-168">Microsoft. ISAM. ESENT. Interop. esentinvalidonsortexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="0a53a-169">Microsoft. ISAM. ESENT. Interop. esentinvalidsystempathexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="0a53a-170">Microsoft. ISAM. ESENT. Interop. esentkeyboundaryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="0a53a-171">Microsoft. ISAM. ESENT. Interop. esentkeyesobigexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="0a53a-172">Microsoft. ISAM. ESENT. Interop. esentlanguagenotsupportedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="0a53a-173">Microsoft. ISAM. ESENT. Interop. esentlinklotsupportedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="0a53a-174">Microsoft. ISAM. ESENT. Interop. esentlogbufferdeosmallexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="0a53a-175">Microsoft. ISAM. ESENT. Interop. esentmissingpatchpageexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="0a53a-176">Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="0a53a-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="0a53a-177">Microsoft. ISAM. ESENT. Interop. esentmustdisableloggingfordbupgradeexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="0a53a-178">Microsoft. ISAM. ESENT. Interop. esentnotindistributedtransaktionexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="0a53a-179">Microsoft. ISAM. ESENT. Interop. esentobjectduplicateexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="0a53a-180">Microsoft. ISAM. ESENT. Interop. esentpageboundaryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="0a53a-181">Microsoft. ISAM. ESENT. Interop. esentpatchfilemissingexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="0a53a-182">Microsoft. ISAM. ESENT. Interop. esentrfsfailureexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="0a53a-183">Microsoft. ISAM. ESENT. Interop. esentrfsnotarmedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="0a53a-184">Microsoft. ISAM. ESENT. Interop. esentrollbackrequirements dexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="0a53a-185">Microsoft. ISAM. ESENT. Interop. esentslvbufferdeosmallexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="0a53a-186">Microsoft. ISAM. ESENT. Interop. esentslvcolumncannotdeleteexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="0a53a-187">Microsoft. ISAM. ESENT. Interop. esentslvcolumndefaultvaluenotallowedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="0a53a-188">Microsoft. ISAM. ESENT. Interop. esentslvbeschädigen tedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="0a53a-189">Microsoft. ISAM. ESENT. Interop. esentslvdatabasemissingexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="0a53a-190">Microsoft. ISAM. ESENT. Interop. esentslvealistkorruptexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="0a53a-191">Microsoft. ISAM. ESENT. Interop. esentslvealistdeobigexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="0a53a-192">Microsoft. ISAM. ESENT. Interop. esentslvealistzerozucationexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="0a53a-193">Microsoft. ISAM. ESENT. Interop. esentslvfileaccessdeniedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="0a53a-194">Microsoft. ISAM. ESENT. Interop. esentslvfilinput useexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="0a53a-195">Microsoft. ISAM. ESENT. Interop. esentslvfileinvalidpathexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="0a53a-196">Microsoft. ISAM. ESENT. Interop. esentslvfileioexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="0a53a-197">Microsoft. ISAM. ESENT. Interop. esentslvfile otfoundexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="0a53a-198">Microsoft. ISAM. ESENT. Interop. esentslvfilestaleexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="0a53a-199">Microsoft. ISAM. ESENT. Interop. esentslvfileunknownexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="0a53a-200">Microsoft. ISAM. ESENT. Interop. esentslvheaderbadchecksumexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="0a53a-201">Microsoft. ISAM. ESENT. Interop. esentslvheaderkorruptedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="0a53a-202">Microsoft. ISAM. ESENT. Interop. esentslvinvalidpathexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="0a53a-203">Microsoft. ISAM. ESENT. Interop. esentslvownermapalleseryexistsexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="0a53a-204">Microsoft. ISAM. ESENT. Interop. esentslvownermapverdertedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="0a53a-205">Microsoft. ISAM. ESENT. Interop. esentslvownermappagenotfoundexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="0a53a-206">Microsoft. ISAM. ESENT. Interop. esentslvpgesnotcommittedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="0a53a-207">Microsoft. ISAM. ESENT. Interop. esentslvpgesnotdeletedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="0a53a-208">Microsoft. ISAM. ESENT. Interop. esentslvpgesnotfreexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="0a53a-209">Microsoft. ISAM. ESENT. Interop. esentslvpgesnotreservedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="0a53a-210">Microsoft. ISAM. ESENT. Interop. esentslvprovidernotloadedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="0a53a-211">Microsoft. ISAM. ESENT. Interop. esentslvproviderversionmismatchexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="0a53a-212">Microsoft. ISAM. ESENT. Interop. esentslvleserverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="0a53a-213">Microsoft. ISAM. ESENT. Interop. esentslvrootnotspecifiedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="0a53a-214">Microsoft. ISAM. ESENT. Interop. esentslvrootpathinvalidexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="0a53a-215">Microsoft. ISAM. ESENT. Interop. esentslvrootstillopenexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="0a53a-216">Microsoft. ISAM. ESENT. Interop. esentslvspacecorruptedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="0a53a-217">Microsoft. ISAM. ESENT. Interop. esentslvspaceschreiteconflictexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="0a53a-218">Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilealleseryexistsexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="0a53a-219">Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilefullexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="0a53a-220">Microsoft. ISAM. ESENT. Interop. esentslvstreamingfileingeuseexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="0a53a-221">Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilemissingexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="0a53a-222">Microsoft. ISAM. ESENT. Interop. esentslvstreamingdaterdatentoedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="0a53a-223">Microsoft. ISAM. ESENT. Interop. esentslvstreamingfilereadonlyexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="0a53a-224">Microsoft. ISAM. ESENT. Interop. esentsoftrecoveryonsnapshotexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="0a53a-225">Microsoft. ISAM. ESENT. Interop. esentspavailextcacheouesschmemoryexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="0a53a-226">Microsoft. ISAM. ESENT. Interop. esentspavailextcacheoudef SyncException</span><span class="sxs-lookup"><span data-stu-id="0a53a-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="0a53a-227">Microsoft. ISAM. ESENT. Interop. esentsqllinklotsupportedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="0a53a-228">Microsoft. ISAM. ESENT. Interop. esentstreamingdatanotloggedexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="0a53a-229">Microsoft. ISAM. ESENT. Interop. esenttaggednotnullexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="0a53a-230">Microsoft. ISAM. ESENT. Interop. esenttempfileopenerrorexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="0a53a-231">Microsoft. ISAM. ESENT. Interop. esentesomanyopendatabasesexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="0a53a-232">Microsoft. ISAM. ESENT. Interop. esentesomanysplitsexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="0a53a-233">Microsoft. ISAM. ESENT. Interop. esentunicodetranslationbufferdeosmallexception</span><span class="sxs-lookup"><span data-stu-id="0a53a-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)