---
description: Legt die Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Signedcode. Description (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373824"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="18b39-103">Signedcode. Description (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18b39-103">SignedCode.Description property</span></span>

<span data-ttu-id="18b39-104">\[Die **Description** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="18b39-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="18b39-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="18b39-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="18b39-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="18b39-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="18b39-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="18b39-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="18b39-108">Die **Description** -Eigenschaft legt die Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="18b39-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b39-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="18b39-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="18b39-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="18b39-110">Property value</span></span>

<span data-ttu-id="18b39-111">Die Beschreibung der signierten ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="18b39-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b39-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18b39-112">Remarks</span></span>

<span data-ttu-id="18b39-113">Die Beschreibung ist der Text, der im Dialogfeld Authenticode-Überprüfung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="18b39-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="18b39-114">Der Text sollte die signierte ausführbare Datei beschreiben.</span><span class="sxs-lookup"><span data-stu-id="18b39-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="18b39-115">Wenn diese Eigenschaft **null** ist, wird im Dialogfeld der Name der ausführbaren Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18b39-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b39-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18b39-116">Requirements</span></span>



| <span data-ttu-id="18b39-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18b39-117">Requirement</span></span> | <span data-ttu-id="18b39-118">Wert</span><span class="sxs-lookup"><span data-stu-id="18b39-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b39-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="18b39-119">Redistributable</span></span><br/> | <span data-ttu-id="18b39-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="18b39-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="18b39-121">DLL</span><span class="sxs-lookup"><span data-stu-id="18b39-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="18b39-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b39-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b39-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b39-124">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="18b39-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
