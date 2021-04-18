---
description: Codiert eine Zeichenfolge als Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. einem base64encode-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366021"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="4ceb2-103">Utilities. einem base64encode-Methode</span><span class="sxs-lookup"><span data-stu-id="4ceb2-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="4ceb2-104">\[Die **einem base64encode** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="4ceb2-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="4ceb2-105">Die **einem base64encode** -Methode codiert eine Zeichenfolge als Base64.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ceb2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ceb2-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="4ceb2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ceb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ceb2-108">*Srcstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ceb2-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ceb2-109">Die Zeichenfolge, die als Base64 codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ceb2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ceb2-110">Return value</span></span>

<span data-ttu-id="4ceb2-111">Die Base64-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ceb2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ceb2-112">Remarks</span></span>

<span data-ttu-id="4ceb2-113">Base64-Codierung ist das Schema, mit dem Binärdaten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="4ceb2-114">Base64 verarbeitet Daten als 24-Bit-Gruppen und ordnet diese Daten vier codierten Zeichen zu.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="4ceb2-115">Base64-Codierung wird manchmal als 3-zu-4-Codierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="4ceb2-116">Jede 6 Bits der 24-Bit-Gruppe wird als Index in einer Mapping-Tabelle (dem Base64-Alphabet) zum Abrufen eines Zeichens für die codierten Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="4ceb2-117">Die codierten Daten weisen Zeilenlängen auf, die auf 76 Zeichen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ceb2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ceb2-118">Requirements</span></span>



| <span data-ttu-id="4ceb2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ceb2-119">Requirement</span></span> | <span data-ttu-id="4ceb2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4ceb2-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ceb2-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4ceb2-121">Redistributable</span></span><br/> | <span data-ttu-id="4ceb2-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ceb2-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ceb2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4ceb2-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="4ceb2-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb2-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ceb2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ceb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ceb2-126">**Versorgungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




