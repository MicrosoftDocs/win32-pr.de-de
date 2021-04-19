---
description: 'Weitere Informationen finden Sie unter: esentoperationexception-Klasse'
title: EsentOperationException-Klasse
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349756"
---
# <a name="esentoperationexception-class"></a><span data-ttu-id="9a464-103">EsentOperationException-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a464-103">EsentOperationException class</span></span>

<span data-ttu-id="9a464-104">Basisklasse für Vorgangs Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="9a464-104">Base class for Operation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9a464-105">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="9a464-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9a464-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9a464-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9a464-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9a464-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9a464-108">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="9a464-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9a464-109">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="9a464-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="9a464-110">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="9a464-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          

<span data-ttu-id="9a464-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a464-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a464-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9a464-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a464-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a464-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="9a464-114">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9a464-114">Thread safety</span></span>

<span data-ttu-id="9a464-115">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="9a464-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9a464-116">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="9a464-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a464-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a464-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a464-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="9a464-118">Reference</span></span>

[<span data-ttu-id="9a464-119">Esentoperationexception-Member</span><span class="sxs-lookup"><span data-stu-id="9a464-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="9a464-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a464-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="9a464-121">Abgeleitete Typen</span><span class="sxs-lookup"><span data-stu-id="9a464-121">Derived types</span></span>

[<span data-ttu-id="9a464-122">System.Object</span><span class="sxs-lookup"><span data-stu-id="9a464-122">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9a464-123">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9a464-123">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9a464-124">Microsoft. ISAM. ESENT. esentexception</span><span class="sxs-lookup"><span data-stu-id="9a464-124">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9a464-125">Microsoft. ISAM. ESENT. Interop. esenterrorexception</span><span class="sxs-lookup"><span data-stu-id="9a464-125">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="9a464-126">Microsoft. ISAM. ESENT. Interop. esentoperationexception</span><span class="sxs-lookup"><span data-stu-id="9a464-126">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          [<span data-ttu-id="9a464-127">Microsoft. ISAM. ESENT. Interop. esentbackupabortbyserverexception</span><span class="sxs-lookup"><span data-stu-id="9a464-127">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>](./esentbackupabortbyserverexception-class.md)  
          [<span data-ttu-id="9a464-128">Microsoft. ISAM. ESENT. Interop. esentcheckpointdepthopodeepexception</span><span class="sxs-lookup"><span data-stu-id="9a464-128">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>](./esentcheckpointdepthtoodeepexception-class.md)  
          [<span data-ttu-id="9a464-129">Microsoft. ISAM. ESENT. Interop. esentclientrequesttostopjetserviceexception</span><span class="sxs-lookup"><span data-stu-id="9a464-129">Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException</span></span>](./esentclientrequesttostopjetserviceexception-class.md)  
          [<span data-ttu-id="9a464-130">Microsoft. ISAM. ESENT. Interop. esentfatalexception</span><span class="sxs-lookup"><span data-stu-id="9a464-130">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
          [<span data-ttu-id="9a464-131">Microsoft. ISAM. ESENT. Interop. esentinitinprogressexception</span><span class="sxs-lookup"><span data-stu-id="9a464-131">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>](./esentinitinprogressexception-class.md)  
          [<span data-ttu-id="9a464-132">Microsoft. ISAM. ESENT. Interop. esentinternalerrorexception</span><span class="sxs-lookup"><span data-stu-id="9a464-132">Microsoft.Isam.Esent.Interop.EsentInternalErrorException</span></span>](./esentinternalerrorexception-class.md)  
          [<span data-ttu-id="9a464-133">Microsoft. ISAM. ESENT. Interop. esentioexception</span><span class="sxs-lookup"><span data-stu-id="9a464-133">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
          [<span data-ttu-id="9a464-134">Microsoft. ISAM. ESENT. Interop. esentntsystemcallfailedexception</span><span class="sxs-lookup"><span data-stu-id="9a464-134">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>](./esentntsystemcallfailedexception-class.md)  
          [<span data-ttu-id="9a464-135">Microsoft. ISAM. ESENT. Interop. esentossnapshottimeoutexception</span><span class="sxs-lookup"><span data-stu-id="9a464-135">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>](./esentossnapshottimeoutexception-class.md)  
          [<span data-ttu-id="9a464-136">Microsoft. ISAM. ESENT. Interop. esentrecordnotdeletedexception</span><span class="sxs-lookup"><span data-stu-id="9a464-136">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>](./esentrecordnotdeletedexception-class.md)  
          [<span data-ttu-id="9a464-137">Microsoft. ISAM. ESENT. Interop. esentresourceexception</span><span class="sxs-lookup"><span data-stu-id="9a464-137">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
          [<span data-ttu-id="9a464-138">Microsoft. ISAM. ESENT. Interop. esentterminprogressexception</span><span class="sxs-lookup"><span data-stu-id="9a464-138">Microsoft.Isam.Esent.Interop.EsentTermInProgressException</span></span>](./esentterminprogressexception-class.md)  
          [<span data-ttu-id="9a464-139">Microsoft. ISAM. ESENT. Interop. esentunicodelta anguagevalidationfailureexception</span><span class="sxs-lookup"><span data-stu-id="9a464-139">Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException</span></span>](./esentunicodelanguagevalidationfailureexception-class.md)  
          [<span data-ttu-id="9a464-140">Microsoft. ISAM. ESENT. Interop. esentunicodetranslationfailexception</span><span class="sxs-lookup"><span data-stu-id="9a464-140">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>](./esentunicodetranslationfailexception-class.md)