---
description: Ruft die Auflistung der Zertifikate in der signierten ausführbaren Datei ab.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Signedcode. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372568"
---
# <a name="signedcodecertificates-property"></a><span data-ttu-id="32049-103">Signedcode. Zertifikats (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="32049-103">SignedCode.Certificates property</span></span>

<span data-ttu-id="32049-104">\[Die Eigenschaft **Zertifikate** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="32049-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="32049-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="32049-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="32049-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="32049-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="32049-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="32049-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="32049-108">Mit der Eigenschaft **Zertifikate** wird die Sammlung der Zertifikate in der signierten ausführbaren Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="32049-108">The **Certificates** property retrieves the collection of certificates in the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="32049-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="32049-109">Syntax</span></span>


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="32049-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="32049-110">Property value</span></span>

<span data-ttu-id="32049-111">Die [**Zertifikats**](certificates.md) Auflistung, die alle Zertifikate in der signierten ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="32049-111">The [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="32049-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32049-112">Requirements</span></span>



| <span data-ttu-id="32049-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32049-113">Requirement</span></span> | <span data-ttu-id="32049-114">Wert</span><span class="sxs-lookup"><span data-stu-id="32049-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32049-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="32049-115">Redistributable</span></span><br/> | <span data-ttu-id="32049-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="32049-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="32049-117">DLL</span><span class="sxs-lookup"><span data-stu-id="32049-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="32049-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32049-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32049-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32049-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32049-120">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="32049-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
