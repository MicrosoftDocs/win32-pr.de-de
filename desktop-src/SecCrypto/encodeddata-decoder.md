---
description: Ruft ein Decoder-Objekt ab, sofern vorhanden.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Encodeddata. Decoder-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367752"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="0ab54-103">Encodeddata. Decoder-Methode</span><span class="sxs-lookup"><span data-stu-id="0ab54-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="0ab54-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0ab54-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0ab54-105">Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0ab54-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0ab54-106">Die **decodermethode** erhält ein Decoder-Objekt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0ab54-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab54-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ab54-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="0ab54-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab54-108">Parameters</span></span>

<span data-ttu-id="0ab54-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ab54-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab54-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ab54-110">Remarks</span></span>

<span data-ttu-id="0ab54-111">Wenn die codierten Daten nicht über ein Decoder-Objekt verfügen, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ab54-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab54-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ab54-112">Requirements</span></span>



| <span data-ttu-id="0ab54-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ab54-113">Requirement</span></span> | <span data-ttu-id="0ab54-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0ab54-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab54-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0ab54-115">End of client support</span></span><br/> | <span data-ttu-id="0ab54-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ab54-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0ab54-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0ab54-117">End of server support</span></span><br/> | <span data-ttu-id="0ab54-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ab54-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0ab54-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0ab54-119">Redistributable</span></span><br/>       | <span data-ttu-id="0ab54-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ab54-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0ab54-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0ab54-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0ab54-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ab54-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
