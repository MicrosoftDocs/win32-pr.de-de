---
description: Legt die URL einer Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Signedcode. DescriptionUrl (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359260"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="ffc39-103">Signedcode. DescriptionUrl (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ffc39-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="ffc39-104">\[Die **DescriptionUrl** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ffc39-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ffc39-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="ffc39-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="ffc39-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffc39-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="ffc39-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="ffc39-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="ffc39-108">Die **DescriptionUrl** -Eigenschaft legt die URL einer Beschreibung der signierten ausführbaren Datei fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="ffc39-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc39-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffc39-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="ffc39-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ffc39-110">Property value</span></span>

<span data-ttu-id="ffc39-111">Die URL einer Beschreibung der signierten ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="ffc39-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffc39-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffc39-112">Remarks</span></span>

<span data-ttu-id="ffc39-113">Die **deskriptionurl** ist die URL, zu der die [**Beschreibung**](signedcode-description.md) im Dialogfeld Authenticode-Überprüfung Links angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ffc39-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="ffc39-114">Wenn diese Eigenschaft **null** ist, kann die **Beschreibung** nicht als Link verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffc39-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffc39-115">Requirements</span></span>



| <span data-ttu-id="ffc39-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffc39-116">Requirement</span></span> | <span data-ttu-id="ffc39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ffc39-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc39-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ffc39-118">Redistributable</span></span><br/> | <span data-ttu-id="ffc39-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="ffc39-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ffc39-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc39-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="ffc39-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc39-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc39-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffc39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc39-123">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="ffc39-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
