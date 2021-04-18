---
description: Gibt einen booleschen Wert zurück, der angibt, ob sich der private Schlüssel in einem Wechsel Speicher befindet.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: PrivateKey. iswechsel-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372630"
---
# <a name="privatekeyisremovable-method"></a><span data-ttu-id="cab1c-103">PrivateKey. iswechsel-Methode</span><span class="sxs-lookup"><span data-stu-id="cab1c-103">PrivateKey.IsRemovable method</span></span>

<span data-ttu-id="cab1c-104">\[Die **iswechsel** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cab1c-104">\[The **IsRemovable** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cab1c-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="cab1c-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cab1c-106">Die **iswechsel** Methode gibt einen booleschen Wert zurück, der angibt, ob sich der private Schlüssel in einem Wechsel Datenträger befindet.</span><span class="sxs-lookup"><span data-stu-id="cab1c-106">The **IsRemovable** method returns a Boolean value that indicates whether the private key is in removable storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab1c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cab1c-107">Syntax</span></span>


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a><span data-ttu-id="cab1c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cab1c-108">Parameters</span></span>

<span data-ttu-id="cab1c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cab1c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cab1c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cab1c-110">Return value</span></span>

<span data-ttu-id="cab1c-111">True gibt an, dass sich der private Schlüssel in Wechselmedien befindet.</span><span class="sxs-lookup"><span data-stu-id="cab1c-111">If true, the private key is in removable storage.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab1c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cab1c-112">Remarks</span></span>

<span data-ttu-id="cab1c-113">Der Rückgabewert dieser Methode ist abhängig vom verwendeten [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP).</span><span class="sxs-lookup"><span data-stu-id="cab1c-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="cab1c-114">Mit dieser Methode wird ein vertrauenswürdiger Wert zurückgegeben, wenn ein Microsoft CSP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cab1c-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="cab1c-115">Wenn es sich bei dem CSP nicht um einen Microsoft CSP handelt, kann der Rückgabewert als nicht vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="cab1c-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab1c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cab1c-116">Requirements</span></span>



| <span data-ttu-id="cab1c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cab1c-117">Requirement</span></span> | <span data-ttu-id="cab1c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cab1c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cab1c-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cab1c-119">Redistributable</span></span><br/> | <span data-ttu-id="cab1c-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="cab1c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cab1c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="cab1c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="cab1c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cab1c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab1c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cab1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab1c-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="cab1c-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
