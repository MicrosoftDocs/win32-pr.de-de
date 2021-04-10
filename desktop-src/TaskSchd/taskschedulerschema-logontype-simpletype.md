---
title: logontype simple-Typ
description: Definiert die möglichen Werte des logontype-Elements.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- logontype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105213"
---
# <a name="logontype-simple-type"></a><span data-ttu-id="12fba-104">logontype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="12fba-104">logonType Simple Type</span></span>

<span data-ttu-id="12fba-105">Definiert die möglichen Werte des [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="12fba-105">Defines the possible values of the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="12fba-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="12fba-106">Enumeration values</span></span>

<span data-ttu-id="12fba-107">Der einfache **logontype** -Typ definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="12fba-107">The **logonType** simple type defines the following values.</span></span>



| <span data-ttu-id="12fba-108">Wert</span><span class="sxs-lookup"><span data-stu-id="12fba-108">Value</span></span>                      | <span data-ttu-id="12fba-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12fba-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fba-110">S4U</span><span class="sxs-lookup"><span data-stu-id="12fba-110">S4U</span></span>                        | <span data-ttu-id="12fba-111">Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden.</span><span class="sxs-lookup"><span data-stu-id="12fba-111">User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="12fba-112">Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.</span><span class="sxs-lookup"><span data-stu-id="12fba-112">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="12fba-113">Kennwort</span><span class="sxs-lookup"><span data-stu-id="12fba-113">Password</span></span>                   | <span data-ttu-id="12fba-114">Der Benutzer muss sich mit einem Kennwort anmelden.</span><span class="sxs-lookup"><span data-stu-id="12fba-114">User must log on using a password.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="12fba-115">Interactivetoken</span><span class="sxs-lookup"><span data-stu-id="12fba-115">InteractiveToken</span></span>           | <span data-ttu-id="12fba-116">Der Benutzer muss bereits angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="12fba-116">User must already be logged on.</span></span> <span data-ttu-id="12fba-117">Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12fba-117">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="12fba-118">Interactiveper kenorpassword</span><span class="sxs-lookup"><span data-stu-id="12fba-118">InteractiveTokenOrPassword</span></span> | <span data-ttu-id="12fba-119">Wird nicht mehr verwendet. aktuell identisch mit dem Kennwort.</span><span class="sxs-lookup"><span data-stu-id="12fba-119">No longer in use; currently identical to Password.</span></span><br/> <span data-ttu-id="12fba-120">**Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista und Windows Server 2008:** Der Task wird in einer vorhandenen interaktiven Sitzung ausgeführt, oder der Benutzer muss sich mit einem Kennwort anmelden.</span><span class="sxs-lookup"><span data-stu-id="12fba-120">**Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista and Windows Server 2008:** The task will be run in an existing interactive session or the user must log on using a password.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="12fba-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12fba-121">Requirements</span></span>



| <span data-ttu-id="12fba-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12fba-122">Requirement</span></span> | <span data-ttu-id="12fba-123">Wert</span><span class="sxs-lookup"><span data-stu-id="12fba-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12fba-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12fba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12fba-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12fba-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12fba-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12fba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12fba-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12fba-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12fba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fba-129">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="12fba-129">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="12fba-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="12fba-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





