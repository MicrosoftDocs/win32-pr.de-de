---
description: Die stationquery-Struktur enthält Informationen zu einem bestimmten Computer, der Netzwerkmonitor verwendet.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Stationquery-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358824"
---
# <a name="stationquery-structure"></a><span data-ttu-id="0df7b-103">Stationquery-Struktur</span><span class="sxs-lookup"><span data-stu-id="0df7b-103">STATIONQUERY structure</span></span>

<span data-ttu-id="0df7b-104">Die **stationquery** -Struktur enthält Informationen zu einem bestimmten Computer, der Netzwerkmonitor verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df7b-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0df7b-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="0df7b-106">Member</span><span class="sxs-lookup"><span data-stu-id="0df7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0df7b-107">**Flags**</span><span class="sxs-lookup"><span data-stu-id="0df7b-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-108">Flags, die den aktuellen Status Netzwerkmonitor identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0df7b-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="0df7b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0df7b-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="0df7b-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0df7b-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="0df7b-111"><dt>**stationquery- \_ Flags \_ geladen**</dt></span><span class="sxs-lookup"><span data-stu-id="0df7b-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="0df7b-112">Der Treiber wird geladen, aber der Kernel ist nicht.</span><span class="sxs-lookup"><span data-stu-id="0df7b-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="0df7b-113"><dt>**stationquery- \_ Flags werden \_ ausgeführt**</dt></span><span class="sxs-lookup"><span data-stu-id="0df7b-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="0df7b-114">Der Treiber ist geladen, aber es werden keine Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="0df7b-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="0df7b-115"><dt>**Aufzeichnen von stationquery- \_ Flags \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df7b-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="0df7b-116">Der Treiber ist aktiv an einer Erfassung beteiligt.</span><span class="sxs-lookup"><span data-stu-id="0df7b-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="0df7b-117"><dt>**Übertragung von stationquery- \_ Flags \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df7b-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="0df7b-118">Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0df7b-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="0df7b-119">**Bcdverminor**</span><span class="sxs-lookup"><span data-stu-id="0df7b-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-120">Die neben Versionsnummer der Netzwerkmonitor, die auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df7b-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-121">**Bcdvermajor**</span><span class="sxs-lookup"><span data-stu-id="0df7b-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-122">Die Hauptversionsnummer der Netzwerkmonitor, die auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df7b-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-123">**Lizenznummer**</span><span class="sxs-lookup"><span data-stu-id="0df7b-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-124">Software Lizenznummer.</span><span class="sxs-lookup"><span data-stu-id="0df7b-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="0df7b-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-126">Der Name des Computer Herstellers, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0df7b-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="0df7b-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-128">Benutzername oder System Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0df7b-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0df7b-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-130">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0df7b-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-131">**Adapteraddress**</span><span class="sxs-lookup"><span data-stu-id="0df7b-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-132">NIC-Adresse</span><span class="sxs-lookup"><span data-stu-id="0df7b-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-133">**Wmachinename**</span><span class="sxs-lookup"><span data-stu-id="0df7b-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-134">Name des Unicode-Computers.</span><span class="sxs-lookup"><span data-stu-id="0df7b-134">Unicode computer name.</span></span> <span data-ttu-id="0df7b-135">Dieser Member gilt für Netzwerkmonitor 2,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0df7b-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="0df7b-136">**Wusername**</span><span class="sxs-lookup"><span data-stu-id="0df7b-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="0df7b-137">Unicode-Benutzername.</span><span class="sxs-lookup"><span data-stu-id="0df7b-137">Unicode user name.</span></span> <span data-ttu-id="0df7b-138">Dieser Member gilt für Netzwerkmonitor 2,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0df7b-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0df7b-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0df7b-139">Remarks</span></span>

<span data-ttu-id="0df7b-140">Ein Array dieser Strukturen wird von der [QueryTable](querytable.md) -Struktur verwendet, um eine Liste der Computer bereitzustellen, die derzeit Netzwerkmonitor zum Erfassen von Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0df7b-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df7b-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0df7b-141">Requirements</span></span>



| <span data-ttu-id="0df7b-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0df7b-142">Requirement</span></span> | <span data-ttu-id="0df7b-143">Wert</span><span class="sxs-lookup"><span data-stu-id="0df7b-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0df7b-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0df7b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0df7b-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0df7b-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0df7b-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0df7b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0df7b-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0df7b-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0df7b-148">Header</span><span class="sxs-lookup"><span data-stu-id="0df7b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df7b-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df7b-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df7b-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0df7b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df7b-151">QueryTable</span><span class="sxs-lookup"><span data-stu-id="0df7b-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 




