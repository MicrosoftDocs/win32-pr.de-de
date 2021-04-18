---
description: Die \_ Bit-Flag-Konstanten von lineaddressmode beschreiben verschiedene Möglichkeiten, eine Adresse auf einem liniengerät zu identifizieren.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372072"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="dee5d-103">Lineaddressmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="dee5d-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="dee5d-104">Die Bit-Flag-Konstanten von **lineaddressmode \_** beschreiben verschiedene Möglichkeiten, eine Adresse auf einem liniengerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dee5d-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="dee5d-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**lineaddressmode \_ -adressssid**</span><span class="sxs-lookup"><span data-stu-id="dee5d-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dee5d-106">Die Adresse wird mit einer kleinen Ganzzahl im Bereich 0 bis *dwnumadkleider* minus 1 angegeben, wobei *dwnumadkleidungs* der Wert in den Gerätefunktionen der Linie ist.</span><span class="sxs-lookup"><span data-stu-id="dee5d-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dee5d-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**lineaddressmode- \_ dialableaddr**</span><span class="sxs-lookup"><span data-stu-id="dee5d-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dee5d-108">Die Adresse wird durch die Telefonnummer angegeben.</span><span class="sxs-lookup"><span data-stu-id="dee5d-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dee5d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dee5d-109">Remarks</span></span>

<span data-ttu-id="dee5d-110">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="dee5d-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="dee5d-111">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="dee5d-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="dee5d-112">Diese Konstante wird verwendet, um eine Adresse in einer Zeile auszuwählen, von der ein-Befehl stammt.</span><span class="sxs-lookup"><span data-stu-id="dee5d-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="dee5d-113">Das übliche Modell wählt die Adresse mithilfe des Adress Bezeichners aus.</span><span class="sxs-lookup"><span data-stu-id="dee5d-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="dee5d-114">Adress Bezeichner sind der Mechanismus, mit dem die Adressen in TAPI identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dee5d-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="dee5d-115">In einigen Umgebungen ist es jedoch oft praktischer, die Ursprungsadresse eines Aufrufs anhand der Telefonnummer anstelle des Adress Bezeichners zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dee5d-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="dee5d-116">Ein Beispiel hierfür ist die Möglichkeit, eine große Anzahl von Stationen (Drittanbieter) auf dem Switch mithilfe eines einzelnen Zeilen Geräts mit vielen Adressen zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="dee5d-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="dee5d-117">Die Linie stellt den Satz aller Stationen dar, und jede Station wird einer Adresse mit ihrer eigenen primären Telefonnummer und Adress Kennung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dee5d-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee5d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dee5d-118">Requirements</span></span>



| <span data-ttu-id="dee5d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dee5d-119">Requirement</span></span> | <span data-ttu-id="dee5d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dee5d-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dee5d-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dee5d-121">TAPI version</span></span><br/> | <span data-ttu-id="dee5d-122">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dee5d-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dee5d-123">Header</span><span class="sxs-lookup"><span data-stu-id="dee5d-123">Header</span></span><br/>       | <dl> <span data-ttu-id="dee5d-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee5d-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




