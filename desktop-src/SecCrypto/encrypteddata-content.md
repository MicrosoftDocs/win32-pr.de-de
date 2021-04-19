---
description: Legt den zu verschlüsselnden oder zu entschlüsselnden Inhalt fest oder ruft ihn ab.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: Verschlüsselteddata. Content (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359229"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="cc4df-103">Verschlüsselteddata. Content (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc4df-103">EncryptedData.Content property</span></span>

<span data-ttu-id="cc4df-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc4df-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cc4df-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="cc4df-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="cc4df-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc4df-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="cc4df-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="cc4df-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="cc4df-108">Die **Content** -Eigenschaft legt den zu verschlüsselnden oder zu entschlüsselnden Inhalt fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cc4df-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="cc4df-109">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc4df-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4df-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc4df-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="cc4df-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cc4df-111">Property value</span></span>

<span data-ttu-id="cc4df-112">Der Inhalt, der verschlüsselt oder entschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc4df-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4df-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc4df-113">Requirements</span></span>



| <span data-ttu-id="cc4df-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc4df-114">Requirement</span></span> | <span data-ttu-id="cc4df-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cc4df-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4df-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cc4df-116">End of client support</span></span><br/> | <span data-ttu-id="cc4df-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc4df-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cc4df-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cc4df-118">End of server support</span></span><br/> | <span data-ttu-id="cc4df-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc4df-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cc4df-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cc4df-120">Redistributable</span></span><br/>       | <span data-ttu-id="cc4df-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc4df-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cc4df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cc4df-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cc4df-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc4df-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4df-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc4df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4df-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="cc4df-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
