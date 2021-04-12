---
description: 'Weitere Informationen finden Sie unter: esentstateexception-Klasse'
title: EsentStateException-Klasse
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218937"
---
# <a name="esentstateexception-class"></a><span data-ttu-id="1fbed-103">EsentStateException-Klasse</span><span class="sxs-lookup"><span data-stu-id="1fbed-103">EsentStateException class</span></span>

<span data-ttu-id="1fbed-104">Basisklasse für Zustands Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="1fbed-104">Base class for State exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1fbed-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="1fbed-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1fbed-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fbed-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1fbed-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1fbed-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1fbed-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1fbed-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1fbed-110">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="1fbed-111">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            

<span data-ttu-id="1fbed-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fbed-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fbed-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fbed-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbed-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fbed-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="1fbed-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="1fbed-115">Thread safety</span></span>

<span data-ttu-id="1fbed-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="1fbed-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1fbed-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="1fbed-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fbed-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fbed-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fbed-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="1fbed-119">Reference</span></span>

[<span data-ttu-id="1fbed-120">Esentstateexception-Member</span><span class="sxs-lookup"><span data-stu-id="1fbed-120">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="1fbed-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fbed-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="1fbed-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="1fbed-122">Derived types</span></span>

[<span data-ttu-id="1fbed-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fbed-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1fbed-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1fbed-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1fbed-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1fbed-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1fbed-127">Microsoft. ISAM. ESENT. Interop. esentapiexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="1fbed-128">Microsoft. ISAM. ESENT. Interop. esentstateexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-128">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            [<span data-ttu-id="1fbed-129">Microsoft. ISAM. ESENT. Interop. esentbackupinprogressexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-129">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>](./esentbackupinprogressexception-class.md)  
            [<span data-ttu-id="1fbed-130">Microsoft. ISAM. ESENT. Interop. esentbackupnotallowedyetexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-130">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>](./esentbackupnotallowedyetexception-class.md)  
            [<span data-ttu-id="1fbed-131">Microsoft. ISAM. ESENT. Interop. esentbaditagsequenceexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-131">Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException</span></span>](./esentbaditagsequenceexception-class.md)  
            [<span data-ttu-id="1fbed-132">Microsoft. ISAM. ESENT. Interop. esentbufferdeosmallexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-132">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>](./esentbuffertoosmallexception-class.md)  
            [<span data-ttu-id="1fbed-133">Microsoft. ISAM. ESENT. Interop. esentcallbackfailedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-133">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>](./esentcallbackfailedexception-class.md)  
            [<span data-ttu-id="1fbed-134">Microsoft. ISAM. ESENT. Interop. esentdatabasealleseryupgradedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-134">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>](./esentdatabasealreadyupgradedexception-class.md)  
            [<span data-ttu-id="1fbed-135">Microsoft. ISAM. ESENT. Interop. esentdatabasefailedinkrementalreseedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-135">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>](./esentdatabasefailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="1fbed-136">Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteupgrade Exception</span><span class="sxs-lookup"><span data-stu-id="1fbed-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>](./esentdatabaseincompleteupgradeexception-class.md)  
            [<span data-ttu-id="1fbed-137">Microsoft. ISAM. ESENT. Interop. esentdatabaseleakinspaceexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>](./esentdatabaseleakinspaceexception-class.md)  
            [<span data-ttu-id="1fbed-138">Microsoft. ISAM. ESENT. Interop. esentdirtyshutdownexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-138">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>](./esentdirtyshutdownexception-class.md)  
            [<span data-ttu-id="1fbed-139">Microsoft. ISAM. ESENT. Interop. esentfilename otfoundexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-139">Microsoft.Isam.Esent.Interop.EsentFileNotFoundException</span></span>](./esentfilenotfoundexception-class.md)  
            [<span data-ttu-id="1fbed-140">Microsoft. ISAM. ESENT. Interop. esentindexinuseexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-140">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>](./esentindexinuseexception-class.md)  
            [<span data-ttu-id="1fbed-141">Microsoft. ISAM. ESENT. Interop. esentindexnotfoundexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-141">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>](./esentindexnotfoundexception-class.md)  
            [<span data-ttu-id="1fbed-142">Microsoft. ISAM. ESENT. Interop. esentinvalidbuffersizeexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-142">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>](./esentinvalidbuffersizeexception-class.md)  
            [<span data-ttu-id="1fbed-143">Microsoft. ISAM. ESENT. Interop. esentinvalidlogdatasequenceexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-143">Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException</span></span>](./esentinvalidlogdatasequenceexception-class.md)  
            [<span data-ttu-id="1fbed-144">Microsoft. ISAM. ESENT. Interop. esentkeyduplicateexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-144">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>](./esentkeyduplicateexception-class.md)  
            [<span data-ttu-id="1fbed-145">Microsoft. ISAM. ESENT. Interop. esentkeytrunalisiedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-145">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>](./esentkeytruncatedexception-class.md)  
            [<span data-ttu-id="1fbed-146">Microsoft. ISAM. ESENT. Interop. EsentLogFileSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1fbed-146">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1fbed-147">Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1fbed-147">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException</span></span>](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1fbed-148">Microsoft. ISAM. ESENT. Interop. esentlsnotsetexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-148">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>](./esentlsnotsetexception-class.md)  
            [<span data-ttu-id="1fbed-149">Microsoft. ISAM. ESENT. Interop. esentmissingfullbackupexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-149">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>](./esentmissingfullbackupexception-class.md)  
            [<span data-ttu-id="1fbed-150">Microsoft. ISAM. ESENT. Interop. esentmultivaluedduplicateaftertruncationexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-150">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [<span data-ttu-id="1fbed-151">Microsoft. ISAM. ESENT. Interop. esentmultivaluedduplicateexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-151">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>](./esentmultivaluedduplicateexception-class.md)  
            [<span data-ttu-id="1fbed-152">Microsoft. ISAM. ESENT. Interop. esentnoattachmentsfailedinkrementalreseedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-152">Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException</span></span>](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="1fbed-153">Microsoft. ISAM. ESENT. Interop. esentnobackupexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-153">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>](./esentnobackupexception-class.md)  
            [<span data-ttu-id="1fbed-154">Microsoft. ISAM. ESENT. Interop. esentnocurrentrecordexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-154">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>](./esentnocurrentrecordexception-class.md)  
            [<span data-ttu-id="1fbed-155">Microsoft. ISAM. ESENT. Interop. esentobjectnotfoundexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-155">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>](./esentobjectnotfoundexception-class.md)  
            [<span data-ttu-id="1fbed-156">Microsoft. ISAM. ESENT. Interop. esentossnapshotnotallowedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-156">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>](./esentossnapshotnotallowedexception-class.md)  
            [<span data-ttu-id="1fbed-157">Microsoft. ISAM. ESENT. Interop. esentrecorddeletedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-157">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>](./esentrecorddeletedexception-class.md)  
            [<span data-ttu-id="1fbed-158">Microsoft. ISAM. ESENT. Interop. esentrecordnotfoundexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-158">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>](./esentrecordnotfoundexception-class.md)  
            [<span data-ttu-id="1fbed-159">Microsoft. ISAM. ESENT. Interop. esentrecorddeobigexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-159">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>](./esentrecordtoobigexception-class.md)  
            [<span data-ttu-id="1fbed-160">Microsoft. ISAM. ESENT. Interop. esentrecordtoobigforbackwardcompatibilityexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-160">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [<span data-ttu-id="1fbed-161">Microsoft. ISAM. ESENT. Interop. esentherstelledwitherrorsexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-161">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>](./esentrecoveredwitherrorsexception-class.md)  
            [<span data-ttu-id="1fbed-162">Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="1fbed-162">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [<span data-ttu-id="1fbed-163">Microsoft. ISAM. ESENT. Interop. esentherstelledwithoutundoexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-163">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>](./esentrecoveredwithoutundoexception-class.md)  
            [<span data-ttu-id="1fbed-164">Microsoft. ISAM. ESENT. Interop. esentrestoreingeprogressexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-164">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>](./esentrestoreinprogressexception-class.md)  
            [<span data-ttu-id="1fbed-165">Microsoft. ISAM. ESENT. Interop. esentseparatedlongvalueexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-165">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>](./esentseparatedlongvalueexception-class.md)  
            [<span data-ttu-id="1fbed-166">Microsoft. ISAM. ESENT. Interop. esentsurrogatebackupinprogressexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-166">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>](./esentsurrogatebackupinprogressexception-class.md)  
            [<span data-ttu-id="1fbed-167">Microsoft. ISAM. ESENT. Interop. esenttableduplicateexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-167">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>](./esenttableduplicateexception-class.md)  
            [<span data-ttu-id="1fbed-168">Microsoft. ISAM. ESENT. Interop. esenttableinuseexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-168">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>](./esenttableinuseexception-class.md)  
            [<span data-ttu-id="1fbed-169">Microsoft. ISAM. ESENT. Interop. esenttestinjectionnotsupportedexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-169">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>](./esenttestinjectionnotsupportedexception-class.md)  
            [<span data-ttu-id="1fbed-170">Microsoft. ISAM. ESENT. Interop. esentschreiteconflictexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-170">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>](./esentwriteconflictexception-class.md)  
            [<span data-ttu-id="1fbed-171">Microsoft. ISAM. ESENT. Interop. esentschreiteconflictprimaryindexexception</span><span class="sxs-lookup"><span data-stu-id="1fbed-171">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>](./esentwriteconflictprimaryindexexception-class.md)