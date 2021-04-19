---
description: Überprüft die Authenticode-Signatur für den signierten Code.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Signedcode. Verify-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370823"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="82d6a-103">Signedcode. Verify-Methode</span><span class="sxs-lookup"><span data-stu-id="82d6a-103">SignedCode.Verify method</span></span>

<span data-ttu-id="82d6a-104">\[Die **Verifizierungs** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="82d6a-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="82d6a-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="82d6a-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="82d6a-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="82d6a-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="82d6a-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="82d6a-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="82d6a-108">Die **Verify** -Methode überprüft die Authenticode-Signatur für den signierten Code.</span><span class="sxs-lookup"><span data-stu-id="82d6a-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d6a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="82d6a-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="82d6a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="82d6a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d6a-111">für den Kauf *zulässig* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="82d6a-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="82d6a-112">Ein boolescher Wert, der angibt, ob ein Dialogfeld verwendet wird, um die Signatur zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="82d6a-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="82d6a-113">True gibt an, dass ein Dialogfeld generiert wird, um zu bestimmen, ob der Code vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="82d6a-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="82d6a-114">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="82d6a-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d6a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82d6a-115">Return value</span></span>

<span data-ttu-id="82d6a-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="82d6a-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d6a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82d6a-117">Requirements</span></span>



| <span data-ttu-id="82d6a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82d6a-118">Requirement</span></span> | <span data-ttu-id="82d6a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="82d6a-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82d6a-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="82d6a-120">Redistributable</span></span><br/> | <span data-ttu-id="82d6a-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="82d6a-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="82d6a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="82d6a-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="82d6a-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d6a-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d6a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82d6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d6a-125">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="82d6a-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
