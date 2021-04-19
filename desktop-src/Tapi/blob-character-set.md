---
description: Die BLOB- \_ Zeichen \_ Satz-Enumeration gibt den Zeichensatz an, der vom aktuellen Konferenz-BLOB verwendet wird.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: BLOB_CHARACTER_SET-Enumeration (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357719"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="31f60-103">BLOB \_ - \_ Zeichensatz-Enumeration</span><span class="sxs-lookup"><span data-stu-id="31f60-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="31f60-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="31f60-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="31f60-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="31f60-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="31f60-106">Die **BLOB- \_ Zeichen \_ Satz** -Enumeration gibt den Zeichensatz an, der vom aktuellen Konferenz-BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31f60-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f60-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f60-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="31f60-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="31f60-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31f60-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS- \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="31f60-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="31f60-110">Standard mäßiges ASCII-Format.</span><span class="sxs-lookup"><span data-stu-id="31f60-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="31f60-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS \_ UTF7**</span><span class="sxs-lookup"><span data-stu-id="31f60-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="31f60-112">Das 7-Bit-Transformations Format von Unicode.</span><span class="sxs-lookup"><span data-stu-id="31f60-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="31f60-113">Ausführliche Informationen zu diesem Format finden Sie unter Durchführen einer Internet Suche nach RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="31f60-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="31f60-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="31f60-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="31f60-115">UCS-Transformations Format 8.</span><span class="sxs-lookup"><span data-stu-id="31f60-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="31f60-116">Ausführliche Informationen zu diesem Format erhalten Sie, wenn Sie eine Internet Suche nach ISO (das internationale Organisation für Normung) und IEC (das Internationale Elektrotechnische Kommission) Dokument ISO/IEC JTC1/SC2/WG2 N 1036, vom 1. August 1994, durch den WG2-Projekt-Editor ausführen.</span><span class="sxs-lookup"><span data-stu-id="31f60-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31f60-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31f60-117">Requirements</span></span>



| <span data-ttu-id="31f60-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31f60-118">Requirement</span></span> | <span data-ttu-id="31f60-119">Wert</span><span class="sxs-lookup"><span data-stu-id="31f60-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31f60-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="31f60-120">TAPI version</span></span><br/> | <span data-ttu-id="31f60-121">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="31f60-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="31f60-122">Header</span><span class="sxs-lookup"><span data-stu-id="31f60-122">Header</span></span><br/>       | <dl> <span data-ttu-id="31f60-123"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f60-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f60-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31f60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f60-125">**Itdirectoryobjectconference**</span><span class="sxs-lookup"><span data-stu-id="31f60-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="31f60-126">**\_Zeichensatz erhalten**</span><span class="sxs-lookup"><span data-stu-id="31f60-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="31f60-127">**Init**</span><span class="sxs-lookup"><span data-stu-id="31f60-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="31f60-128">**Setconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="31f60-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




