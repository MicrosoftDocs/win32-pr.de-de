---
description: Löscht den Zertifikat Speicher, der durch das aktuelle Speicher Objekt dargestellt wird.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360456"
---
# <a name="storedelete-method"></a><span data-ttu-id="088f7-103">Store. Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="088f7-103">Store.Delete method</span></span>

<span data-ttu-id="088f7-104">\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="088f7-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="088f7-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="088f7-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="088f7-106">Mit der **Delete** -Methode wird der [*Zertifikat Speicher*](../secgloss/c-gly.md) gelöscht, der durch das aktuelle [**Speicher**](certificate.md) Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="088f7-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="088f7-107">Mit dieser Methode werden nur nicht-Systemspeicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="088f7-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="088f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="088f7-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="088f7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="088f7-109">Parameters</span></span>

<span data-ttu-id="088f7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="088f7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="088f7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="088f7-111">Return value</span></span>

<span data-ttu-id="088f7-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="088f7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="088f7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="088f7-113">Remarks</span></span>

<span data-ttu-id="088f7-114">Die folgenden Speicher sind Systemspeicher und können nicht gelöscht werden:</span><span class="sxs-lookup"><span data-stu-id="088f7-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="088f7-115">My</span><span class="sxs-lookup"><span data-stu-id="088f7-115">My</span></span>
-   <span data-ttu-id="088f7-116">Root</span><span class="sxs-lookup"><span data-stu-id="088f7-116">Root</span></span>
-   <span data-ttu-id="088f7-117">Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="088f7-117">Trust</span></span>
-   <span data-ttu-id="088f7-118">CA</span><span class="sxs-lookup"><span data-stu-id="088f7-118">CA</span></span>
-   <span data-ttu-id="088f7-119">Userds</span><span class="sxs-lookup"><span data-stu-id="088f7-119">UserDS</span></span>
-   <span data-ttu-id="088f7-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="088f7-120">TrustedPublisher</span></span>
-   <span data-ttu-id="088f7-121">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="088f7-121">Disallowed</span></span>
-   <span data-ttu-id="088f7-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="088f7-122">AuthRoot</span></span>
-   <span data-ttu-id="088f7-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="088f7-123">TrustedPeople</span></span>

<span data-ttu-id="088f7-124">Die **Delete** -Methode gibt einen Fehler zurück, wenn Sie von einem Webskript aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="088f7-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="088f7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="088f7-125">Requirements</span></span>



| <span data-ttu-id="088f7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="088f7-126">Requirement</span></span> | <span data-ttu-id="088f7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="088f7-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="088f7-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="088f7-128">Redistributable</span></span><br/> | <span data-ttu-id="088f7-129">CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="088f7-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="088f7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="088f7-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="088f7-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088f7-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088f7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="088f7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088f7-133">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="088f7-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="088f7-134">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="088f7-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
