---
description: Gibt eine Zeichen folgen Darstellung der codierten Daten zurück.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Encodeddata. Format-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370281"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="64fed-103">Encodeddata. Format-Methode</span><span class="sxs-lookup"><span data-stu-id="64fed-103">EncodedData.Format method</span></span>

<span data-ttu-id="64fed-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64fed-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="64fed-105">Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="64fed-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="64fed-106">Die **Format** -Methode gibt eine Zeichen folgen Darstellung der codierten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="64fed-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="64fed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64fed-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="64fed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64fed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64fed-109">*bmultilines* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="64fed-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="64fed-110">Boolescher Wert, der angibt, ob die zurückgegebene Zeichenfolge mehrere Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="64fed-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="64fed-111">**True** gibt an, dass die zurückgegebene Zeichenfolge mehrere Zeilen enthalten kann, die durch **vbCrLf** getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="64fed-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="64fed-112">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="64fed-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64fed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64fed-113">Return value</span></span>

<span data-ttu-id="64fed-114">Eine lesbare Zeichenfolge, die die codierten Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="64fed-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="64fed-115">Wenn CAPICOM die codierten Daten nicht versteht, wird eine hexadezimale Darstellung der Daten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64fed-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="64fed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64fed-116">Remarks</span></span>

<span data-ttu-id="64fed-117">Das Format der zurückgegebenen Zeichenfolge kann sich zwischen verschiedenen Versionen von CAPICOM ändern.</span><span class="sxs-lookup"><span data-stu-id="64fed-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="64fed-118">Verlassen Sie sich nicht auf ein bestimmtes Format in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="64fed-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="64fed-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64fed-119">Requirements</span></span>



| <span data-ttu-id="64fed-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64fed-120">Requirement</span></span> | <span data-ttu-id="64fed-121">Wert</span><span class="sxs-lookup"><span data-stu-id="64fed-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64fed-122">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="64fed-122">End of client support</span></span><br/> | <span data-ttu-id="64fed-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64fed-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="64fed-124">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="64fed-124">End of server support</span></span><br/> | <span data-ttu-id="64fed-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64fed-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="64fed-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="64fed-126">Redistributable</span></span><br/>       | <span data-ttu-id="64fed-127">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="64fed-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="64fed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="64fed-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="64fed-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64fed-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64fed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64fed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fed-131">**Encoddata**</span><span class="sxs-lookup"><span data-stu-id="64fed-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
