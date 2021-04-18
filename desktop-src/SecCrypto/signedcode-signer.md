---
description: Ruft den Signatur Geber der signierten ausführbaren Datei ab.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Signedcode. Signer (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371647"
---
# <a name="signedcodesigner-property"></a><span data-ttu-id="65e84-103">Signedcode. Signer (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="65e84-103">SignedCode.Signer property</span></span>

<span data-ttu-id="65e84-104">\[Die **Signatur** Geber Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="65e84-104">\[The **Signer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65e84-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="65e84-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="65e84-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="65e84-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="65e84-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="65e84-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="65e84-108">Die **Signatur** Geber-Eigenschaft ruft den Signatur Geber der signierten ausführbaren Datei ab.</span><span class="sxs-lookup"><span data-stu-id="65e84-108">The **Signer** property retrieves the signer of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e84-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e84-109">Syntax</span></span>


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a><span data-ttu-id="65e84-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="65e84-110">Property value</span></span>

<span data-ttu-id="65e84-111">Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Signatur Geber der signierten ausführbaren Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="65e84-111">A [**Signer**](signer.md) object that provides access to the signer of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e84-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65e84-112">Requirements</span></span>



| <span data-ttu-id="65e84-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65e84-113">Requirement</span></span> | <span data-ttu-id="65e84-114">Wert</span><span class="sxs-lookup"><span data-stu-id="65e84-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65e84-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="65e84-115">Redistributable</span></span><br/> | <span data-ttu-id="65e84-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="65e84-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="65e84-117">DLL</span><span class="sxs-lookup"><span data-stu-id="65e84-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="65e84-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65e84-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e84-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65e84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e84-120">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="65e84-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
