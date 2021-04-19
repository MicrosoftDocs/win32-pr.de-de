---
description: Die timestamper-Eigenschaft ruft den Zeitstempel der signierten ausführbaren Datei ab.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Signedcode. timestamper-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365792"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="8ed15-103">Signedcode. timestamper-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ed15-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="8ed15-104">\[Die **timestamper** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8ed15-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8ed15-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="8ed15-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="8ed15-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ed15-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="8ed15-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="8ed15-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="8ed15-108">Die **timestamper** -Eigenschaft ruft den Zeitstempel der signierten ausführbaren Datei ab.</span><span class="sxs-lookup"><span data-stu-id="8ed15-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed15-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ed15-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="8ed15-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8ed15-110">Property value</span></span>

<span data-ttu-id="8ed15-111">Ein [**Signatur**](signer.md) Geber Objekt, das Zugriff auf den Zeitstempel der signierten ausführbaren Datei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ed15-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed15-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ed15-112">Requirements</span></span>



| <span data-ttu-id="8ed15-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ed15-113">Requirement</span></span> | <span data-ttu-id="8ed15-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8ed15-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed15-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8ed15-115">Redistributable</span></span><br/> | <span data-ttu-id="8ed15-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8ed15-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8ed15-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8ed15-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8ed15-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ed15-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed15-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ed15-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed15-120">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="8ed15-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
