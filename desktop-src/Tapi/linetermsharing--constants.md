---
description: Die linetermsharing- \_ Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen ein Terminal von Zeilen Geräten, Adressen oder Aufrufen gemeinsam genutzt werden kann.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: LINETERMSHARING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366019"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="5f117-103">Linetermsharing- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="5f117-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="5f117-104">Die **linetermsharing \_** -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen ein Terminal von Zeilen Geräten, Adressen oder Aufrufen gemeinsam genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f117-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="5f117-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**linetermsharing \_ Privat**</span><span class="sxs-lookup"><span data-stu-id="5f117-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f117-106">Das Terminal Gerät ist für ein einzeilige Gerät privat.</span><span class="sxs-lookup"><span data-stu-id="5f117-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f117-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**linetermsharing \_ sharedconf**</span><span class="sxs-lookup"><span data-stu-id="5f117-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f117-108">Das Terminal Gerät kann von mehreren Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f117-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="5f117-109">Die [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) -Anforderungen der verschiedenen Terminals werden am Terminal zusammengeführt oder am Terminal übertragen.</span><span class="sxs-lookup"><span data-stu-id="5f117-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5f117-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**linetermsharing \_ sharedexcl**</span><span class="sxs-lookup"><span data-stu-id="5f117-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5f117-111">Das Terminal Gerät kann von mehreren Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f117-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="5f117-112">Das letzte Zeilen Gerät, für das ein [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) oder [**TSPI \_ linesetterminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) mit dem Terminal für einen bestimmten Terminal Modus ausgeführt wird, verfügt über eine exklusive Verbindung mit dem Terminal für diesen Modus.</span><span class="sxs-lookup"><span data-stu-id="5f117-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f117-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f117-113">Remarks</span></span>

<span data-ttu-id="5f117-114">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="5f117-114">No extensibility.</span></span> <span data-ttu-id="5f117-115">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="5f117-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="5f117-116">Diese Konstanten beschreiben die Klassen von Steuerungs-und Informationsdaten strömen, die direkt zwischen einem Linien Gerät und einem Terminal Gerät (z. b. einem Telefon Satz) weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="5f117-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f117-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f117-117">Requirements</span></span>



| <span data-ttu-id="5f117-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f117-118">Requirement</span></span> | <span data-ttu-id="5f117-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5f117-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5f117-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5f117-120">TAPI version</span></span><br/> | <span data-ttu-id="5f117-121">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5f117-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5f117-122">Header</span><span class="sxs-lookup"><span data-stu-id="5f117-122">Header</span></span><br/>       | <dl> <span data-ttu-id="5f117-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f117-123"><dt>Tapi.h</dt></span></span> </dl> |



 

