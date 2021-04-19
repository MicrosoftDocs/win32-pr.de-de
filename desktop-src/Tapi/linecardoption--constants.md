---
description: Die linecardoption- \_ Konstanten definieren Werte, die im dwOptions-Member der linecardentry-Struktur verwendet werden, die als Teil der linetranslatecaps-Struktur zurückgegeben wird, die von linegettranslatecaps zurückgegeben wurde.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: LINECARDOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370857"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="b79f0-103">Linecardoption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="b79f0-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="b79f0-104">Die **linecardoption \_ -Konstanten** definieren Werte, die im **dwOptions** -Member der [**linecardentry**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) -Struktur verwendet werden, die als Teil der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur zurückgegeben wird, die von [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b79f0-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="b79f0-105">Die **linecardoption- \_ Konstanten** t weisen die folgenden Werte auf:</span><span class="sxs-lookup"><span data-stu-id="b79f0-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b79f0-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**linecardoption \_ ausgeblendet**</span><span class="sxs-lookup"><span data-stu-id="b79f0-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b79f0-107">Diese Aufruf Karte wurde vom Benutzer ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b79f0-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="b79f0-108">Sie wird in der Haupt Auflistung der verfügbaren Aufruf Karten nicht durch das Dial-Hilfsobjekt angezeigt, wird jedoch in der Liste der Karten angezeigt, von denen die Regeln zum abwählen kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b79f0-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b79f0-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**linecardoption \_ vordefiniert**</span><span class="sxs-lookup"><span data-stu-id="b79f0-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b79f0-110">Diese Aufruf Karte ist eine der vordefinierten Aufruf Karten Definitionen, die von Microsoft in der Telefoniekarte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b79f0-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="b79f0-111">Sie kann nicht vollständig mithilfe von Dial Helper entfernt werden. Wenn der Benutzer versucht, ihn zu entfernen, wird er ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b79f0-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="b79f0-112">Auf diese Weise ist der Zugriff auf das Kopieren von Wähl Regeln weiterhin möglich.</span><span class="sxs-lookup"><span data-stu-id="b79f0-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b79f0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b79f0-113">Remarks</span></span>

<span data-ttu-id="b79f0-114">Nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="b79f0-114">Not extensible.</span></span> <span data-ttu-id="b79f0-115">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="b79f0-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79f0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b79f0-116">Requirements</span></span>



| <span data-ttu-id="b79f0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b79f0-117">Requirement</span></span> | <span data-ttu-id="b79f0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b79f0-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b79f0-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b79f0-119">TAPI version</span></span><br/> | <span data-ttu-id="b79f0-120">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b79f0-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b79f0-121">Header</span><span class="sxs-lookup"><span data-stu-id="b79f0-121">Header</span></span><br/>       | <dl> <span data-ttu-id="b79f0-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79f0-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




