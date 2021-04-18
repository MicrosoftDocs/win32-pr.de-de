---
description: Ruft den Algorithmus für die verschlüsselten Daten ab.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: Verschlüsselteddata. algorithmuseigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360913"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="321e5-103">Verschlüsselteddata. algorithmuseigenschaft</span><span class="sxs-lookup"><span data-stu-id="321e5-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="321e5-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="321e5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="321e5-105">Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="321e5-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="321e5-106">Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="321e5-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="321e5-107">Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]</span><span class="sxs-lookup"><span data-stu-id="321e5-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="321e5-108">Die  algorithmuseigenschaft Ruft den Algorithmus für die verschlüsselten Daten ab.</span><span class="sxs-lookup"><span data-stu-id="321e5-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="321e5-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="321e5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="321e5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="321e5-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="321e5-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="321e5-111">Property value</span></span>

<span data-ttu-id="321e5-112">Ein [**Algorithmusobjekt**](algorithm.md) , das den Verschlüsselungsalgorithmus darstellt.</span><span class="sxs-lookup"><span data-stu-id="321e5-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="321e5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="321e5-113">Requirements</span></span>



| <span data-ttu-id="321e5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="321e5-114">Requirement</span></span> | <span data-ttu-id="321e5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="321e5-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="321e5-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="321e5-116">End of client support</span></span><br/> | <span data-ttu-id="321e5-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="321e5-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="321e5-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="321e5-118">End of server support</span></span><br/> | <span data-ttu-id="321e5-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="321e5-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="321e5-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="321e5-120">Redistributable</span></span><br/>       | <span data-ttu-id="321e5-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="321e5-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="321e5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="321e5-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="321e5-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321e5-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321e5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321e5-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="321e5-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
