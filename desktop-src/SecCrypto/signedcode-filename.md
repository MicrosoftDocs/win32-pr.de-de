---
description: Die FileName-Eigenschaft legt den Pfad zur ausführbaren Datei fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Signedcode. filename (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362170"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="a1aea-104">Signedcode. filename (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a1aea-104">SignedCode.FileName property</span></span>

<span data-ttu-id="a1aea-105">\[Die **filename** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a1aea-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1aea-106">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="a1aea-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="a1aea-107">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1aea-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="a1aea-108">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="a1aea-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="a1aea-109">Die **filename** -Eigenschaft legt den Pfad zur ausführbaren Datei fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="a1aea-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="a1aea-110">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a1aea-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1aea-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1aea-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="a1aea-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a1aea-112">Property value</span></span>

<span data-ttu-id="a1aea-113">Der Pfad zur ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="a1aea-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1aea-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1aea-114">Remarks</span></span>

<span data-ttu-id="a1aea-115">Wenn der Wert der **filename** -Eigenschaft geändert wird, wird der Status des gesamten [**signedcode**](signedcode.md) -Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a1aea-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1aea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1aea-116">Requirements</span></span>



| <span data-ttu-id="a1aea-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1aea-117">Requirement</span></span> | <span data-ttu-id="a1aea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a1aea-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1aea-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a1aea-119">Redistributable</span></span><br/> | <span data-ttu-id="a1aea-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1aea-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a1aea-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a1aea-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="a1aea-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1aea-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1aea-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1aea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1aea-124">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="a1aea-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
