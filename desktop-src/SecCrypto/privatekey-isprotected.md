---
description: Gibt einen booleschen Wert zurück, der angibt, ob der private Schlüssel geschützt ist.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: PrivateKey. IsProtected-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371234"
---
# <a name="privatekeyisprotected-method"></a><span data-ttu-id="c5e68-103">PrivateKey. IsProtected-Methode</span><span class="sxs-lookup"><span data-stu-id="c5e68-103">PrivateKey.IsProtected method</span></span>

<span data-ttu-id="c5e68-104">\[Die **IsProtected** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c5e68-104">\[The **IsProtected** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5e68-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c5e68-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c5e68-106">Die **IsProtected** -Methode gibt einen booleschen Wert zurück, der angibt, ob der private Schlüssel geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="c5e68-106">The **IsProtected** method returns a Boolean value that indicates whether the private key is protected.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e68-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e68-107">Syntax</span></span>


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a><span data-ttu-id="c5e68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e68-108">Parameters</span></span>

<span data-ttu-id="c5e68-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c5e68-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5e68-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5e68-110">Return value</span></span>

<span data-ttu-id="c5e68-111">True gibt an, dass der private Schlüssel geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="c5e68-111">If true, the private key is protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5e68-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5e68-112">Remarks</span></span>

<span data-ttu-id="c5e68-113">Der Rückgabewert dieser Methode ist abhängig vom verwendeten [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP).</span><span class="sxs-lookup"><span data-stu-id="c5e68-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="c5e68-114">Mit dieser Methode wird ein vertrauenswürdiger Wert zurückgegeben, wenn ein Microsoft CSP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5e68-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="c5e68-115">Wenn es sich bei dem CSP nicht um einen Microsoft CSP handelt, kann der Rückgabewert als nicht vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="c5e68-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e68-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5e68-116">Requirements</span></span>



| <span data-ttu-id="c5e68-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5e68-117">Requirement</span></span> | <span data-ttu-id="c5e68-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c5e68-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e68-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c5e68-119">Redistributable</span></span><br/> | <span data-ttu-id="c5e68-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5e68-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5e68-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c5e68-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="c5e68-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5e68-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e68-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5e68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e68-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="c5e68-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
