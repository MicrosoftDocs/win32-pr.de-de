---
description: Die linespecialinfo \_ -Bitflag-Konstanten beschreiben besondere Informationen, die das Netzwerk verwenden kann, um verschiedene Vorgänge zur Berichterstellung und Netzwerküberwachung zu melden.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: LINESPECIALINFO_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358032"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="9c6e4-103">Linespecialinfo- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="9c6e4-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="9c6e4-104">Die **linespecialinfo \_** -Bitflag-Konstanten beschreiben besondere Informationen, die das Netzwerk verwenden kann, um verschiedene Vorgänge zur Berichterstellung und Netzwerküberwachung zu melden.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="9c6e4-105">Dabei handelt es sich um spezielle codierte Audiosequenzen, die am Anfang der aufgezeichneten Ankündigungen der Netzwerkberatung übertragen werden</span><span class="sxs-lookup"><span data-stu-id="9c6e4-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="9c6e4-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**linespecialinfo \_ custirreg**</span><span class="sxs-lookup"><span data-stu-id="9c6e4-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c6e4-107">Dieser besondere Informations Ton liegt vor einer leeren Zahl, einem AIS, einer Centrex-Nummer und einer nicht funktionierenden Station, dem Zugriffs Code, der nicht gewählt wurde oder bei dem ein Fehler auftritt, oder der manuellen Abfang Operator-Nachricht (Kategorie der Kunden Unregelmäßigkeiten).</span><span class="sxs-lookup"><span data-stu-id="9c6e4-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="9c6e4-108">Linespecialinfo \_ custirreg wird auch gemeldet, wenn die Abrechnungsinformationen abgelehnt werden und die IP-Adresse am Switch blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c6e4-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**linespecialinfo- \_ nocircuit**</span><span class="sxs-lookup"><span data-stu-id="9c6e4-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c6e4-110">Dieser besondere Informations Ton geht vor einer keinen Verbindung oder einer Notfall Ankündigung (trunk Blockierung hin-Kategorie).</span><span class="sxs-lookup"><span data-stu-id="9c6e4-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c6e4-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**linespecialinfo \_ neu anordnen**</span><span class="sxs-lookup"><span data-stu-id="9c6e4-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c6e4-112">Dieser besondere Informations Ton geht vor einer Neuanordnungs Ankündigung (Kategorie der Kategorie der Geräte).</span><span class="sxs-lookup"><span data-stu-id="9c6e4-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="9c6e4-113">Linespecialinfo \_ reorder wird auch gemeldet, wenn das Telefon zu lange offline gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c6e4-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**linespecialinfo ist \_ nicht verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="9c6e4-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c6e4-115">Einzelheiten zum speziellen Informations Ton sind nicht verfügbar und werden nicht bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c6e4-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**linespecialinfo \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="9c6e4-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c6e4-117">Einzelheiten zum speziellen Informations Ton sind zurzeit unbekannt, werden aber später möglicherweise bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c6e4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c6e4-118">Remarks</span></span>

<span data-ttu-id="9c6e4-119">Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="9c6e4-120">Die nieder wertigen 16 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="9c6e4-121">Besondere Informations Töne werden für Beratungs Nachrichten definiert und in der Regel nicht für Abrechnungs-oder Aufsichts Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c6e4-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c6e4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c6e4-122">Requirements</span></span>



| <span data-ttu-id="9c6e4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c6e4-123">Requirement</span></span> | <span data-ttu-id="9c6e4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9c6e4-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9c6e4-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="9c6e4-125">TAPI version</span></span><br/> | <span data-ttu-id="9c6e4-126">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9c6e4-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9c6e4-127">Header</span><span class="sxs-lookup"><span data-stu-id="9c6e4-127">Header</span></span><br/>       | <dl> <span data-ttu-id="9c6e4-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6e4-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




