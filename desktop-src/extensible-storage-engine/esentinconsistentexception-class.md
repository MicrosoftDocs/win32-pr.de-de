---
description: 'Weitere Informationen finden Sie unter: EsentInconsistentException-Klasse'
title: EsentInconsistentException-Klasse
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106351833"
---
# <a name="esentinconsistentexception-class"></a><span data-ttu-id="134d9-103">EsentInconsistentException-Klasse</span><span class="sxs-lookup"><span data-stu-id="134d9-103">EsentInconsistentException class</span></span>

<span data-ttu-id="134d9-104">Basisklasse für inkonsistente Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="134d9-104">Base class for Inconsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="134d9-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="134d9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="134d9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="134d9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="134d9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="134d9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="134d9-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="134d9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="134d9-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="134d9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="134d9-110">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="134d9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="134d9-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="134d9-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            

<span data-ttu-id="134d9-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="134d9-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="134d9-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="134d9-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="134d9-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="134d9-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="134d9-115">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="134d9-115">Thread safety</span></span>

<span data-ttu-id="134d9-116">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="134d9-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="134d9-117">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="134d9-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="134d9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="134d9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="134d9-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="134d9-119">Reference</span></span>

[<span data-ttu-id="134d9-120">EsentInconsistentException-Member</span><span class="sxs-lookup"><span data-stu-id="134d9-120">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="134d9-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="134d9-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="134d9-122">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="134d9-122">Derived types</span></span>

[<span data-ttu-id="134d9-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="134d9-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="134d9-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="134d9-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="134d9-125">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="134d9-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="134d9-126">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="134d9-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="134d9-127">Microsoft. ISAM. ESENT. Interop. esentdataexception</span><span class="sxs-lookup"><span data-stu-id="134d9-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="134d9-128">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="134d9-128">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            [<span data-ttu-id="134d9-129">Microsoft. ISAM. ESENT. Interop. esentattacheddatabasemismatchexception</span><span class="sxs-lookup"><span data-stu-id="134d9-129">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>](./esentattacheddatabasemismatchexception-class.md)  
            [<span data-ttu-id="134d9-130">Microsoft. ISAM. ESENT. Interop. esentbadcheckpointsignatureexception</span><span class="sxs-lookup"><span data-stu-id="134d9-130">Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException</span></span>](./esentbadcheckpointsignatureexception-class.md)  
            [<span data-ttu-id="134d9-131">Microsoft. ISAM. ESENT. Interop. esentbadlogsignatureexception</span><span class="sxs-lookup"><span data-stu-id="134d9-131">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>](./esentbadlogsignatureexception-class.md)  
            [<span data-ttu-id="134d9-132">Microsoft. ISAM. ESENT. Interop. esentbadlogversionexception</span><span class="sxs-lookup"><span data-stu-id="134d9-132">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>](./esentbadlogversionexception-class.md)  
            [<span data-ttu-id="134d9-133">Microsoft. ISAM. ESENT. Interop. esentcheckpointfile topics-Quelle</span><span class="sxs-lookup"><span data-stu-id="134d9-133">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>](./esentcheckpointfilenotfoundexception-class.md)  
            [<span data-ttu-id="134d9-134">Microsoft. ISAM. ESENT. Interop. esentkonsistenttimemismatchexception</span><span class="sxs-lookup"><span data-stu-id="134d9-134">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>](./esentconsistenttimemismatchexception-class.md)  
            [<span data-ttu-id="134d9-135">Microsoft. ISAM. ESENT. Interop. esentdatabasedirtyshutdownexception</span><span class="sxs-lookup"><span data-stu-id="134d9-135">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>](./esentdatabasedirtyshutdownexception-class.md)  
            [<span data-ttu-id="134d9-136">Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteinkrementalreseedexception</span><span class="sxs-lookup"><span data-stu-id="134d9-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [<span data-ttu-id="134d9-137">Microsoft. ISAM. ESENT. Interop. esentdatabaselogsetmismatchexception</span><span class="sxs-lookup"><span data-stu-id="134d9-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException</span></span>](./esentdatabaselogsetmismatchexception-class.md)  
            [<span data-ttu-id="134d9-138">Microsoft. ISAM. ESENT. Interop. esentdbtimedeonewexception</span><span class="sxs-lookup"><span data-stu-id="134d9-138">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>](./esentdbtimetoonewexception-class.md)  
            [<span data-ttu-id="134d9-139">Microsoft. ISAM. ESENT. Interop. esentdbtimedeooldexception</span><span class="sxs-lookup"><span data-stu-id="134d9-139">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>](./esentdbtimetoooldexception-class.md)  
            [<span data-ttu-id="134d9-140">Microsoft. ISAM. ESENT. Interop. esentendingrestorelogopolowexception</span><span class="sxs-lookup"><span data-stu-id="134d9-140">Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException</span></span>](./esentendingrestorelogtoolowexception-class.md)  
            [<span data-ttu-id="134d9-141">Microsoft. ISAM. ESENT. Interop. esentexistinglogfilehasbadsignatureexception</span><span class="sxs-lookup"><span data-stu-id="134d9-141">Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException</span></span>](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="134d9-142">Microsoft. ISAM. ESENT. Interop. esentexistinglogfileisnotcontiguousexception</span><span class="sxs-lookup"><span data-stu-id="134d9-142">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="134d9-143">Microsoft. ISAM. ESENT. Interop. esentfileinvalidtypeexception</span><span class="sxs-lookup"><span data-stu-id="134d9-143">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>](./esentfileinvalidtypeexception-class.md)  
            [<span data-ttu-id="134d9-144">Microsoft. ISAM. ESENT. Interop. esentgivenlogfilehasbadsignatureexception</span><span class="sxs-lookup"><span data-stu-id="134d9-144">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="134d9-145">Microsoft. ISAM. ESENT. Interop. esentgivenlogfileisnotcontiguousexception</span><span class="sxs-lookup"><span data-stu-id="134d9-145">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="134d9-146">Microsoft. ISAM. ESENT. Interop. esentinvalidkreatedbversionexception</span><span class="sxs-lookup"><span data-stu-id="134d9-146">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>](./esentinvalidcreatedbversionexception-class.md)  
            [<span data-ttu-id="134d9-147">Microsoft. ISAM. ESENT. Interop. esentinvaliddatabaseversionexception</span><span class="sxs-lookup"><span data-stu-id="134d9-147">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>](./esentinvaliddatabaseversionexception-class.md)  
            [<span data-ttu-id="134d9-148">Microsoft. ISAM. ESENT. Interop. esentloggenerationmismatchexception</span><span class="sxs-lookup"><span data-stu-id="134d9-148">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>](./esentloggenerationmismatchexception-class.md)  
            [<span data-ttu-id="134d9-149">Microsoft. ISAM. ESENT. Interop. esentmissingcurrentlogfilesexception</span><span class="sxs-lookup"><span data-stu-id="134d9-149">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>](./esentmissingcurrentlogfilesexception-class.md)  
            [<span data-ttu-id="134d9-150">Microsoft. ISAM. ESENT. Interop. esentmissingfilebackbackupexception</span><span class="sxs-lookup"><span data-stu-id="134d9-150">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>](./esentmissingfiletobackupexception-class.md)  
            [<span data-ttu-id="134d9-151">Microsoft. ISAM. ESENT. Interop. esentmissingrestorelogfilesexception</span><span class="sxs-lookup"><span data-stu-id="134d9-151">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>](./esentmissingrestorelogfilesexception-class.md)  
            [<span data-ttu-id="134d9-152">Microsoft. ISAM. ESENT. Interop. esentpagesizemismatchexception</span><span class="sxs-lookup"><span data-stu-id="134d9-152">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>](./esentpagesizemismatchexception-class.md)  
            [<span data-ttu-id="134d9-153">Microsoft. ISAM. ESENT. Interop. esentrequirements dlogfilesmissingexception</span><span class="sxs-lookup"><span data-stu-id="134d9-153">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>](./esentrequiredlogfilesmissingexception-class.md)  
            [<span data-ttu-id="134d9-154">Microsoft. ISAM. ESENT. Interop. esentstartingrestorelogesohighexception</span><span class="sxs-lookup"><span data-stu-id="134d9-154">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>](./esentstartingrestorelogtoohighexception-class.md)