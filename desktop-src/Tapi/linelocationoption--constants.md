---
description: Die linelocationoption- \_ Konstanten definieren Werte, die im dwOptions-Member der linelocationentry-Struktur verwendet werden, die als Teil der linetranslatecaps-Struktur zurückgegeben wird, die von linegettranslatecaps zurückgegeben wurde.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372653"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="1bbae-103">Linelocationoption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="1bbae-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="1bbae-104">Die **linelocationoption \_** -Konstanten definieren Werte, die im **dwOptions** -Member der [**linelocationentry**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) -Struktur verwendet werden, die als Teil der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur zurückgegeben wird, die von [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1bbae-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="1bbae-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**linelocationoption \_ Pull Dial**</span><span class="sxs-lookup"><span data-stu-id="1bbae-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1bbae-106">Der standardmäßige Wähl Modus an diesem Speicherort ist Pulse Wähl.</span><span class="sxs-lookup"><span data-stu-id="1bbae-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="1bbae-107">Wenn dieses Bit festgelegt ist, fügt [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) einen "P"-Wähl Modifizierer an den Anfang der als DFÜ-Zeichenfolge zurückgegebenen Zeichenfolge ein, wenn dieser Speicherort ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1bbae-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="1bbae-108">Wenn dieses Bit nicht festgelegt ist, fügt **linetranslateaddress** einen "T"-wählmodifizierer am Anfang der DFÜ-Zeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="1bbae-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bbae-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bbae-109">Remarks</span></span>

<span data-ttu-id="1bbae-110">Nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="1bbae-110">Not extensible.</span></span> <span data-ttu-id="1bbae-111">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="1bbae-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bbae-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bbae-112">Requirements</span></span>



| <span data-ttu-id="1bbae-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bbae-113">Requirement</span></span> | <span data-ttu-id="1bbae-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1bbae-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1bbae-115">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1bbae-115">TAPI version</span></span><br/> | <span data-ttu-id="1bbae-116">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1bbae-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1bbae-117">Header</span><span class="sxs-lookup"><span data-stu-id="1bbae-117">Header</span></span><br/>       | <dl> <span data-ttu-id="1bbae-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bbae-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




