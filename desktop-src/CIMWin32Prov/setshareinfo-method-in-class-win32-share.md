---
description: Der setshareingefo-&\# 8194; WMI-Klassenmethode legt die Parameter einer freigegebenen Ressource fest.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Setshareingefo-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214295"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="68441-103">Setshareingefo-Methode der Win32- \_ Freigabe Klasse</span><span class="sxs-lookup"><span data-stu-id="68441-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="68441-104">Die **setshareinfo** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode legt die Parameter einer freigegebenen Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="68441-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="68441-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="68441-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="68441-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="68441-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="68441-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="68441-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="68441-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68441-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68441-109">*MaximumAllowed* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="68441-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68441-110">Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="68441-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="68441-111">Beispiel: 10.</span><span class="sxs-lookup"><span data-stu-id="68441-111">Example: 10.</span></span> <span data-ttu-id="68441-112">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="68441-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="68441-113">*Beschreibung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="68441-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68441-114">Optionaler Kommentar zum Beschreiben der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="68441-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="68441-115">*Zugriff* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="68441-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68441-116">Sicherheits Beschreibung für Berechtigungen auf Benutzerebene.</span><span class="sxs-lookup"><span data-stu-id="68441-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="68441-117">Eine Sicherheits Beschreibung enthält Informationen zu den Berechtigungen, den Besitzern und den Zugriffs Funktionen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="68441-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="68441-118">Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="68441-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68441-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68441-119">Return value</span></span>

<span data-ttu-id="68441-120">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="68441-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="68441-121">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="68441-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68441-122">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="68441-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68441-123">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="68441-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="68441-124">**Ungültiger Name** (9)</span><span class="sxs-lookup"><span data-stu-id="68441-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="68441-125">**Ungültige Ebene** (10)</span><span class="sxs-lookup"><span data-stu-id="68441-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="68441-126">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="68441-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="68441-127">**Doppelte Freigabe** (22)</span><span class="sxs-lookup"><span data-stu-id="68441-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="68441-128">**Umgeleiteter Pfad** (23)</span><span class="sxs-lookup"><span data-stu-id="68441-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="68441-129">**Unbekanntes Gerät oder Verzeichnis** (24)</span><span class="sxs-lookup"><span data-stu-id="68441-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="68441-130">Der **Netzwerkname wurde nicht gefunden** (25).</span><span class="sxs-lookup"><span data-stu-id="68441-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="68441-131">**Sonstige** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="68441-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="68441-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68441-132">Remarks</span></span>

<span data-ttu-id="68441-133">Die **setshareinfo** -Methode ist eine dynamische Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="68441-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="68441-134">Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Konto Operatoren" oder die Gruppenmitgliedschaften "Kommunikation", "Drucken" oder "Server Operator" können " **setshareinfo**" erfolgreich ausführen</span><span class="sxs-lookup"><span data-stu-id="68441-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="68441-135">Der Druck Operator kann nur Drucker Warteschlangen festlegen.</span><span class="sxs-lookup"><span data-stu-id="68441-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="68441-136">Der Kommunikations Operator kann nur Warteschlangen für Kommunikationsgeräte festlegen.</span><span class="sxs-lookup"><span data-stu-id="68441-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="68441-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68441-137">Examples</span></span>

<span data-ttu-id="68441-138">Im folgenden PowerShell-Beispiel wird der Name der **NewShare** -Freigabe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="68441-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="68441-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68441-139">Requirements</span></span>



| <span data-ttu-id="68441-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68441-140">Requirement</span></span> | <span data-ttu-id="68441-141">Wert</span><span class="sxs-lookup"><span data-stu-id="68441-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68441-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68441-142">Minimum supported client</span></span><br/> | <span data-ttu-id="68441-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68441-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68441-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68441-144">Minimum supported server</span></span><br/> | <span data-ttu-id="68441-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68441-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68441-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="68441-146">Namespace</span></span><br/>                | <span data-ttu-id="68441-147">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68441-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68441-148">MOF</span><span class="sxs-lookup"><span data-stu-id="68441-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68441-149"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="68441-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68441-150">DLL</span><span class="sxs-lookup"><span data-stu-id="68441-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68441-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68441-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68441-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68441-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="68441-153">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68441-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="68441-154">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="68441-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

