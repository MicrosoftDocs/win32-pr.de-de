---
description: Decodiert eine Zeichenfolge aus base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Utilities. Base64Decode-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364708"
---
# <a name="utilitiesbase64decode-method"></a><span data-ttu-id="09420-103">Utilities. Base64Decode-Methode</span><span class="sxs-lookup"><span data-stu-id="09420-103">Utilities.Base64Decode method</span></span>

<span data-ttu-id="09420-104">\[Die **Base64Decode** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="09420-104">\[The **Base64Decode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="09420-105">Die **Base64Decode** -Methode decodiert eine Zeichenfolge aus base64.</span><span class="sxs-lookup"><span data-stu-id="09420-105">The **Base64Decode** method decodes a string from base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="09420-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09420-106">Syntax</span></span>


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a><span data-ttu-id="09420-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="09420-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09420-108">*Encodstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09420-108">*EncodedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09420-109">Die zu decodierende base64-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="09420-109">The base64-encoded string to decode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09420-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09420-110">Return value</span></span>

<span data-ttu-id="09420-111">Die decodierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="09420-111">The decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="09420-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09420-112">Remarks</span></span>

<span data-ttu-id="09420-113">Base64-Codierung ist das Schema, mit dem Binärdaten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="09420-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="09420-114">Base64 verarbeitet Daten als 24-Bit-Gruppen und ordnet diese Daten vier codierten Zeichen zu.</span><span class="sxs-lookup"><span data-stu-id="09420-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="09420-115">Base64-Codierung wird manchmal als 3-zu-4-Codierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="09420-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="09420-116">Jede 6 Bits der 24-Bit-Gruppe wird als Index in einer Mapping-Tabelle (dem Base64-Alphabet) zum Abrufen eines Zeichens für die codierten Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="09420-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="09420-117">Die codierten Daten weisen Zeilenlängen auf, die auf 76 Zeichen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="09420-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="09420-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09420-118">Requirements</span></span>



| <span data-ttu-id="09420-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09420-119">Requirement</span></span> | <span data-ttu-id="09420-120">Wert</span><span class="sxs-lookup"><span data-stu-id="09420-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09420-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="09420-121">Redistributable</span></span><br/> | <span data-ttu-id="09420-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="09420-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09420-123">DLL</span><span class="sxs-lookup"><span data-stu-id="09420-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="09420-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09420-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09420-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09420-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09420-126">**Versorgungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="09420-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




