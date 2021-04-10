---
description: Erstellt eine neue Win32- \_ clustershare-Instanz.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Create-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127649"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="8db57-103">Create-Methode der Win32 \_ clustershare-Klasse</span><span class="sxs-lookup"><span data-stu-id="8db57-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="8db57-104">Erstellt eine neue [**Win32- \_ clustershare**](win32-clustershare.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="8db57-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8db57-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="8db57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db57-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8db57-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-108">Lokaler Pfad der Windows-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="8db57-108">Local path of the Windows share.</span></span>

<span data-ttu-id="8db57-109">Beispiel: "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="8db57-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="8db57-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8db57-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-111">Der Alias für einen Pfad, der als Freigabe auf einem Computersystem eingerichtet wird, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8db57-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="8db57-112">Beispiel: "Public".</span><span class="sxs-lookup"><span data-stu-id="8db57-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="8db57-113">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8db57-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-114">Der Typ der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="8db57-114">Type of resource being shared.</span></span> <span data-ttu-id="8db57-115">Zu den Typen zählen: Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.</span><span class="sxs-lookup"><span data-stu-id="8db57-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="8db57-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8db57-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-117">Laufwerk</span><span class="sxs-lookup"><span data-stu-id="8db57-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="8db57-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8db57-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-119">Druckwarteschlange</span><span class="sxs-lookup"><span data-stu-id="8db57-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="8db57-120">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="8db57-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-121">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="8db57-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="8db57-122">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="8db57-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-123">IPC</span><span class="sxs-lookup"><span data-stu-id="8db57-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="8db57-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="8db57-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-125">Laufwerks Administrator</span><span class="sxs-lookup"><span data-stu-id="8db57-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="8db57-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="8db57-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-127">Drucker Warteschlangen Administrator</span><span class="sxs-lookup"><span data-stu-id="8db57-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="8db57-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="8db57-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-129">Geräte Administrator</span><span class="sxs-lookup"><span data-stu-id="8db57-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="8db57-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="8db57-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="8db57-131">IPC-Administrator</span><span class="sxs-lookup"><span data-stu-id="8db57-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8db57-132">*MaximumAllowed* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8db57-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-133">Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="8db57-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="8db57-134">*Beschreibung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8db57-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-135">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8db57-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8db57-136">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8db57-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-137">TBD</span><span class="sxs-lookup"><span data-stu-id="8db57-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="8db57-138">*Zugriff* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8db57-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8db57-139">Optionale eingebettete Instanz einer [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse, die die Sicherheits Beschreibung für die neue Freigabe enthält.</span><span class="sxs-lookup"><span data-stu-id="8db57-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8db57-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8db57-140">Requirements</span></span>



| <span data-ttu-id="8db57-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8db57-141">Requirement</span></span> | <span data-ttu-id="8db57-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8db57-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8db57-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8db57-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8db57-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8db57-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="8db57-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8db57-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8db57-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8db57-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8db57-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="8db57-147">Namespace</span></span><br/>                | <span data-ttu-id="8db57-148">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8db57-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8db57-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8db57-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8db57-150"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8db57-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8db57-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8db57-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db57-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db57-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db57-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8db57-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db57-154">**Win32- \_ clustershare**</span><span class="sxs-lookup"><span data-stu-id="8db57-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

