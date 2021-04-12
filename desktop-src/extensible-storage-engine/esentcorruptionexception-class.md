---
description: 'Weitere Informationen finden Sie unter: esentverdertionexception-Klasse'
title: EsentCorruptionException-Klasse
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218939"
---
# <a name="esentcorruptionexception-class"></a><span data-ttu-id="74e3f-103">EsentCorruptionException-Klasse</span><span class="sxs-lookup"><span data-stu-id="74e3f-103">EsentCorruptionException class</span></span>

<span data-ttu-id="74e3f-104">Basisklasse für Beschädigungen von Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="74e3f-104">Base class for Corruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="74e3f-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="74e3f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="74e3f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="74e3f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="74e3f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="74e3f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="74e3f-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="74e3f-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="74e3f-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="74e3f-111">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            

<span data-ttu-id="74e3f-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="74e3f-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="74e3f-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="74e3f-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="74e3f-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="74e3f-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="74e3f-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="74e3f-115">Thread safety</span></span>

<span data-ttu-id="74e3f-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="74e3f-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="74e3f-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="74e3f-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="74e3f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74e3f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74e3f-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="74e3f-119">Reference</span></span>

[<span data-ttu-id="74e3f-120">Esentverdertionexception-Member</span><span class="sxs-lookup"><span data-stu-id="74e3f-120">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="74e3f-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="74e3f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="74e3f-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="74e3f-122">Derived types</span></span>

[<span data-ttu-id="74e3f-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="74e3f-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="74e3f-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="74e3f-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="74e3f-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="74e3f-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="74e3f-127">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="74e3f-128">Microsoft. ISAM. ESENT. Interop. esentverdertionexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-128">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            [<span data-ttu-id="74e3f-129">Microsoft. ISAM. ESENT. Interop. esentbademptypageexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-129">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>](./esentbademptypageexception-class.md)  
            [<span data-ttu-id="74e3f-130">Microsoft. ISAM. ESENT. Interop. esentbadpagelinkexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-130">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>](./esentbadpagelinkexception-class.md)  
            [<span data-ttu-id="74e3f-131">Microsoft. ISAM. ESENT. Interop. esentbadparentpagelinkexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-131">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>](./esentbadparentpagelinkexception-class.md)  
            [<span data-ttu-id="74e3f-132">Microsoft. ISAM. ESENT. Interop. esentcatalogverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-132">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>](./esentcatalogcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-133">Microsoft. ISAM. ESENT. Interop. esentcheckpointbeschädigen TException</span><span class="sxs-lookup"><span data-stu-id="74e3f-133">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>](./esentcheckpointcorruptexception-class.md)  
            [<span data-ttu-id="74e3f-134">Microsoft. ISAM. ESENT. Interop. esentcommittedlogfilebeschädigen TException</span><span class="sxs-lookup"><span data-stu-id="74e3f-134">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>](./esentcommittedlogfilecorruptexception-class.md)  
            [<span data-ttu-id="74e3f-135">Microsoft. ISAM. ESENT. Interop. esentcommittedlogfilesmissingexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-135">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>](./esentcommittedlogfilesmissingexception-class.md)  
            [<span data-ttu-id="74e3f-136">Microsoft. ISAM. ESENT. Interop. esentdatabasebufferdependenciescorruptedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-136">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-137">Microsoft. ISAM. ESENT. Interop. esentdatabasecorruptedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-137">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>](./esentdatabasecorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-138">Microsoft. ISAM. ESENT. Interop. esentdbtimeverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-138">Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException</span></span>](./esentdbtimecorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-139">Microsoft. ISAM. ESENT. Interop. EsentDecompressionFailedException</span><span class="sxs-lookup"><span data-stu-id="74e3f-139">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>](./esentdecompressionfailedexception-class.md)  
            [<span data-ttu-id="74e3f-140">Microsoft. ISAM. ESENT. Interop. esentderivedcolumnkorruptionexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-140">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>](./esentderivedcolumncorruptionexception-class.md)  
            [<span data-ttu-id="74e3f-141">Microsoft. ISAM. ESENT. Interop. esentdiskleseverificationfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-141">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>](./esentdiskreadverificationfailureexception-class.md)  
            [<span data-ttu-id="74e3f-142">Microsoft. ISAM. ESENT. Interop. esentfileiobeyonentofexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-142">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>](./esentfileiobeyondeofexception-class.md)  
            [<span data-ttu-id="74e3f-143">Microsoft. ISAM. ESENT. Interop. esentfilesystemkorruptionexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-143">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>](./esentfilesystemcorruptionexception-class.md)  
            [<span data-ttu-id="74e3f-144">Microsoft. ISAM. ESENT. Interop. esentindexbuildverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-144">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>](./esentindexbuildcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-145">Microsoft. ISAM. ESENT. Interop. esentinvalidlogsequenceexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-145">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>](./esentinvalidlogsequenceexception-class.md)  
            [<span data-ttu-id="74e3f-146">Microsoft. ISAM. ESENT. Interop. esentlogkorruptduringhardrecoveryexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-146">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="74e3f-147">Microsoft. ISAM. ESENT. Interop. esentlogkorruptduringhardrestoreexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-147">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>](./esentlogcorruptduringhardrestoreexception-class.md)  
            [<span data-ttu-id="74e3f-148">Microsoft. ISAM. ESENT. Interop. esentlogkorruptedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-148">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>](./esentlogcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-149">Microsoft. ISAM. ESENT. Interop. esentlogfilebeschädigen TException</span><span class="sxs-lookup"><span data-stu-id="74e3f-149">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>](./esentlogfilecorruptexception-class.md)  
            [<span data-ttu-id="74e3f-150">Microsoft. ISAM. ESENT. Interop. esentlogreadverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-150">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>](./esentlogreadverifyfailureexception-class.md)  
            [<span data-ttu-id="74e3f-151">Microsoft. ISAM. ESENT. Interop. esentlogtornschreiteduringhardrecoveryexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-151">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="74e3f-152">Microsoft. ISAM. ESENT. Interop. esentlogtornschreiteduringhardrestoreexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-152">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [<span data-ttu-id="74e3f-153">Microsoft. ISAM. ESENT. Interop. esentlvverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-153">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>](./esentlvcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-154">Microsoft. ISAM. ESENT. Interop. esentmissinglogfileexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-154">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>](./esentmissinglogfileexception-class.md)  
            [<span data-ttu-id="74e3f-155">Microsoft. ISAM. ESENT. Interop. esentmissingpreviouslogfileexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-155">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>](./esentmissingpreviouslogfileexception-class.md)  
            [<span data-ttu-id="74e3f-156">Microsoft. ISAM. ESENT. Interop. esentpagenotinitializedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-156">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>](./esentpagenotinitializedexception-class.md)  
            [<span data-ttu-id="74e3f-157">Microsoft. ISAM. ESENT. Interop. esentprimaryindexverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-157">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>](./esentprimaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-158">Microsoft. ISAM. ESENT. Interop. esentlelostflushverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-158">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>](./esentreadlostflushverifyfailureexception-class.md)  
            [<span data-ttu-id="74e3f-159">Microsoft. ISAM. ESENT. Interop. esentlupgnoverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-159">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>](./esentreadpgnoverifyfailureexception-class.md)  
            [<span data-ttu-id="74e3f-160">Microsoft. ISAM. ESENT. Interop. esentleserverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-160">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>](./esentreadverifyfailureexception-class.md)  
            [<span data-ttu-id="74e3f-161">Microsoft. ISAM. ESENT. Interop. esentrecordformatsubversionfailedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-161">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>](./esentrecordformatconversionfailedexception-class.md)  
            [<span data-ttu-id="74e3f-162">Microsoft. ISAM. ESENT. Interop. esentherstellyverifyfailureexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-162">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>](./esentrecoveryverifyfailureexception-class.md)  
            [<span data-ttu-id="74e3f-163">Microsoft. ISAM. ESENT. Interop. esentredoabruptendedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-163">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>](./esentredoabruptendedexception-class.md)  
            [<span data-ttu-id="74e3f-164">Microsoft. ISAM. ESENT. Interop. esentsecondaryindexverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-164">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>](./esentsecondaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-165">Microsoft. ISAM. ESENT. Interop. esentspavailextverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-165">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>](./esentspavailextcorruptedexception-class.md)  
            [<span data-ttu-id="74e3f-166">Microsoft. ISAM. ESENT. Interop. esentspownextverdertedexception</span><span class="sxs-lookup"><span data-stu-id="74e3f-166">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>](./esentspownextcorruptedexception-class.md)