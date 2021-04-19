---
description: Erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der signedcode. FileName-Eigenschaft angegeben ist.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Signedcode. Timestamp-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359361"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="1e17f-103">Signedcode. Timestamp-Methode</span><span class="sxs-lookup"><span data-stu-id="1e17f-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="1e17f-104">\[Die **timestamp** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1e17f-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e17f-105">Verwenden Sie stattdessen den Platform invoations Dienst (PInvoke) zum Aufrufen der Win32-API [**signersignetx**](signersignex.md)-, [**signertimestampex**](signertimestampex.md)-und [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Funktionen, um Inhalte mit einer digitalen Authenticode-Signatur zu signieren.</span><span class="sxs-lookup"><span data-stu-id="1e17f-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="1e17f-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="1e17f-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1e17f-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="1e17f-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1e17f-108">Die **timestamp** -Methode erstellt eine Authenticode-Zeitstempel Signatur für die signierte ausführbare Datei, die in der **signedcode. filename** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1e17f-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="1e17f-109">Dieser Zeitstempel ist eine gegen Signatur der signierten ausführbaren Datei, die von einer Zeitstempel Zertifizierungsstelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e17f-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e17f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e17f-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="1e17f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e17f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e17f-112">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e17f-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e17f-113">Eine Zeichenfolge, die die URL des Zeitstempel Servers enthält.</span><span class="sxs-lookup"><span data-stu-id="1e17f-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e17f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e17f-114">Return value</span></span>

<span data-ttu-id="1e17f-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e17f-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e17f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e17f-116">Remarks</span></span>

<span data-ttu-id="1e17f-117">Ein Zeitstempel verlängert die Gültigkeit eines Zertifikats, indem überprüft wird, ob die ausführbare Datei zum Zeitpunkt der Zeitstempel signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e17f-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="1e17f-118">Bevor diese Methode aufgerufen werden kann, muss die signierte ausführbare Datei, die mit einem Zeitstempel versehen werden soll, in der **signedcode. filename** -Eigenschaft angegeben werden, und die [**signedcode. Sign**](signedcode-sign.md) -Methode muss zum Signieren der ausführbaren Datei aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1e17f-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="1e17f-119">Wenn die signierte ausführbare Datei bereits mit einem Zeitstempel versehen ist, überschreibt diese Methode den vorhandenen Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="1e17f-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e17f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e17f-120">Requirements</span></span>



| <span data-ttu-id="1e17f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e17f-121">Requirement</span></span> | <span data-ttu-id="1e17f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1e17f-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e17f-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1e17f-123">Redistributable</span></span><br/> | <span data-ttu-id="1e17f-124">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e17f-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1e17f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1e17f-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="1e17f-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e17f-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e17f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e17f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e17f-128">**Signedcode**</span><span class="sxs-lookup"><span data-stu-id="1e17f-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
