---
title: PDU-Typwerte (SNMP. h)
description: Die PDU-Typwerte werden im PDU- \_ type-Feld des PDU verwendet, um den Typ zu beschreiben.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478432"
---
# <a name="pdu-type-values"></a><span data-ttu-id="1173b-103">PDU-Typwerte</span><span class="sxs-lookup"><span data-stu-id="1173b-103">PDU Type Values</span></span>

<span data-ttu-id="1173b-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1173b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1173b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1173b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1173b-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="1173b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="1173b-107">Die PDU-Typwerte werden im **PDU- \_ Type** -Feld des PDU verwendet, um den Typ zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1173b-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="1173b-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="1173b-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="1173b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1173b-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="1173b-110"><dt>**SNMP \_ PDU \_ Get**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="1173b-111">Suchen und Abrufen eines Werts aus einer angegebenen SNMP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1173b-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="1173b-112"><dt>**SNMP \_ PDU \_ GetNext**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="1173b-113">Suchen und rufen Sie den Wert einer SNMP-Variablen ab, ohne den genauen Namen der Variablen zu kennen.</span><span class="sxs-lookup"><span data-stu-id="1173b-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="1173b-114"><dt>**SNMP- \_ PDU- \_ Antwort**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="1173b-115">Antworten Sie auf eine SNMP \_ PDU \_ Get-oder SNMP \_ PDU \_ GetNext-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1173b-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="1173b-116"><dt>**SNMP- \_ PDU- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="1173b-117">Speichert einen Wert in einer angegebenen SNMP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1173b-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="1173b-118"><dt>**SNMP \_ PDU \_ V1TRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="1173b-119">Gibt an, dass die PDU-Trap so formatiert ist, dass Sie dem SNMPv1-Standard entspricht.</span><span class="sxs-lookup"><span data-stu-id="1173b-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="1173b-120"><dt>**SNMP \_ PDU \_ Getbulk**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="1173b-121">Durchsuchen und Abrufen mehrerer Werte mit einer einzelnen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1173b-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="1173b-122"><dt>**SNMP \_ PDU- \_ Information**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="1173b-123">Gibt eine anforderungsanforderungs-PDU an.</span><span class="sxs-lookup"><span data-stu-id="1173b-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="1173b-124"><dt>**SNMP- \_ PDU- \_ Trap**</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="1173b-125">Benachrichtigt das Verwaltungssystem auf ein außergewöhnliches Ereignis unter SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="1173b-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="1173b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1173b-126">Requirements</span></span>



| <span data-ttu-id="1173b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1173b-127">Requirement</span></span> | <span data-ttu-id="1173b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1173b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1173b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1173b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1173b-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1173b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="1173b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1173b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1173b-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1173b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1173b-133">Header</span><span class="sxs-lookup"><span data-stu-id="1173b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1173b-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="1173b-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1173b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1173b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1173b-136">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="1173b-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="1173b-137">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="1173b-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="1173b-138">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="1173b-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

