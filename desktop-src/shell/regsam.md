---
description: Ein Datentyp, der zum Angeben der Sicherheits Zugriffs Attribute in der Registrierung verwendet wird.
title: Regsam (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983085"
---
# <a name="regsam"></a><span data-ttu-id="a799a-103">Regsam</span><span class="sxs-lookup"><span data-stu-id="a799a-103">REGSAM</span></span>

<span data-ttu-id="a799a-104">Ein Datentyp, der zum Angeben der Sicherheits Zugriffs Attribute in der Registrierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a799a-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="a799a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="a799a-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="a799a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a799a-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="a799a-107"><dt>**Schlüssel \_ \_ Zugriff**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="a799a-108">Kombination \* \* \* \* Key \_ Query \_ value \* \* \* \*, \* \* \* \* Key \_ Enumerate \_ Sub \_ Keys \* \* \* \*, \* \* \* \* Key \_ Notify \* \* \* \*, \* \* \* \* Key \_ Create \_ Sub \_ Key \* \* \* \*, \* \* \* \* Key \_ Create \_ Link \* \* \* \* und \* \* \* \* Key \_ Set \_ value \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="a799a-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="a799a-109"><dt>**\_Link zum Erstellen von Schlüsseln \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="a799a-110">Berechtigung zum Erstellen eines symbolischen Links.</span><span class="sxs-lookup"><span data-stu-id="a799a-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="a799a-111"><dt>**Key \_ Create \_ Sub \_ Key**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="a799a-112">Berechtigung zum Erstellen von unter Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a799a-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="a799a-113"><dt>**Schlüssel \_ \_ Unterschlüssel aufzählen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="a799a-114">Berechtigung zum Aufzählen von unter Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a799a-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="a799a-115"><dt>**Schlüssel \_ Ausführung**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="a799a-116">Berechtigung für Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="a799a-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="a799a-117"><dt>**Schlüssel \_ Benachrichtigung**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="a799a-118">Berechtigung für Änderungs Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a799a-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="a799a-119"><dt>**Schlüssel \_ Abfrage \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="a799a-120">Berechtigung zum Abfragen von Unterschlüssel Daten.</span><span class="sxs-lookup"><span data-stu-id="a799a-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="a799a-121"><dt>**Schlüssel \_ Lesevorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="a799a-122">Kombination aus \* \* \* \* Key \_ Query \_ value \* \* \* \*, \* \* \* \* Key \_ Enumerate \_ Sub \_ Keys \* \* \* \* und \* \* \* \* Key \_ Notify \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="a799a-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="a799a-123"><dt>**Schlüssel \_ Satz \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="a799a-124">Berechtigung zum Festlegen von Unterschlüssel Daten.</span><span class="sxs-lookup"><span data-stu-id="a799a-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="a799a-125"><dt>**Schlüssel \_ Schreibvorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="a799a-126">Kombination aus \* \* \* \* Key \_ Set \_ Value \* \* \* \* und \* \* \* \* Key \_ Create \_ Sub \_ Key \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="a799a-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="a799a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a799a-127">Remarks</span></span>

<span data-ttu-id="a799a-128">Bei einem **regsam** -Wert kann es sich um einen oder mehrere der aufgelisteten Werte handeln.</span><span class="sxs-lookup"><span data-stu-id="a799a-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a799a-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a799a-129">Requirements</span></span>



| <span data-ttu-id="a799a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a799a-130">Requirement</span></span> | <span data-ttu-id="a799a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a799a-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a799a-132">Header</span><span class="sxs-lookup"><span data-stu-id="a799a-132">Header</span></span><br/> | <dl> <span data-ttu-id="a799a-133"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a799a-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




