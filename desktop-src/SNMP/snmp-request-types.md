---
title: SNMP-Anforderungs Typen (SNMP. h)
description: Die SNMP-Anforderungs Typen werden verwendet, um den Vorgang zu beschreiben, der vom SNMP-Dienst für die Ausführung angefordert wird.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478429"
---
# <a name="snmp-request-types"></a><span data-ttu-id="55e39-103">SNMP-Anforderungs Typen</span><span class="sxs-lookup"><span data-stu-id="55e39-103">SNMP Request Types</span></span>

<span data-ttu-id="55e39-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="55e39-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55e39-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="55e39-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="55e39-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="55e39-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="55e39-107">Die SNMP-Anforderungs Typen werden verwendet, um den Vorgang zu beschreiben, der vom SNMP-Dienst für die Ausführung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="55e39-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="55e39-108">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="55e39-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="55e39-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55e39-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="55e39-110"><dt>**SNMP \_ Erweiterung \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="55e39-111">Ruft den Wert der Werte der angegebenen Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="55e39-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="55e39-112"><dt>**SNMP \_ Erweiterung \_ get \_ Next**</dt> <dt>SNMP \_ PDU \_ GetNext</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="55e39-113">Ruft den Wert oder die Werte des lexikografischen Nachfolgers der angegebenen Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="55e39-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="55e39-114"><dt>**SNMP \_ Erweiterung \_ get \_ Bulk**</dt> <dt>SNMP \_ PDU \_ Getbulk</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="55e39-115">Durchsuchen und Abrufen mehrerer Werte mit einer einzelnen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="55e39-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="55e39-116"><dt>**SNMP- \_ Erweiterungs \_ Satz \_ Test**</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="55e39-117">Überprüfen Sie die Werte der angegebenen Variablen.</span><span class="sxs-lookup"><span data-stu-id="55e39-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="55e39-118">Dieser Vorgang maximiert die Wahrscheinlichkeit eines erfolgreichen Schreibvorgangs während der commitanforderung.</span><span class="sxs-lookup"><span data-stu-id="55e39-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="55e39-119">Weitere Informationen finden Sie in der Funktion [**snmpextensionqueryex**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="55e39-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="55e39-120"><dt>**SNMP \_ Erweiterungs \_ Satz \_ Commit**</dt> für <dt>SNMP- \_ PDU \_ festgelegt</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="55e39-121">Schreiben Sie die neuen Werte in die angegebenen Variablen.</span><span class="sxs-lookup"><span data-stu-id="55e39-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="55e39-122"><dt>**SNMP- \_ Erweiterungs \_ Satz \_ rückgängig machen**</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="55e39-123">Setzen Sie die Werte der angegebenen Variablen auf ihre Werte vor der Commit-Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="55e39-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="55e39-124"><dt>**Cleanup für SNMP- \_ Erweiterungs \_ Satz \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="55e39-125">Geben Sie die in vorherigen Anforderungen und Vorgängen zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="55e39-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="55e39-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55e39-126">Requirements</span></span>



| <span data-ttu-id="55e39-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55e39-127">Requirement</span></span> | <span data-ttu-id="55e39-128">Wert</span><span class="sxs-lookup"><span data-stu-id="55e39-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55e39-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55e39-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55e39-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55e39-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="55e39-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55e39-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55e39-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55e39-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55e39-133">Header</span><span class="sxs-lookup"><span data-stu-id="55e39-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="55e39-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e39-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e39-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55e39-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e39-136">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="55e39-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="55e39-137">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="55e39-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="55e39-138">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="55e39-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

