---
description: Listet die aktuell definierten ACE-Typen auf.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (WinNT. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347953"
---
# <a name="ace"></a><span data-ttu-id="b6ade-103">Spezialisierung</span><span class="sxs-lookup"><span data-stu-id="b6ade-103">ACE</span></span>

<span data-ttu-id="b6ade-104">Ein **ACE** ist ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) in einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL).</span><span class="sxs-lookup"><span data-stu-id="b6ade-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="b6ade-105">In der folgenden Tabelle sind die aktuell definierten **ACE** -Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6ade-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6ade-106">ACE-Typ</span><span class="sxs-lookup"><span data-stu-id="b6ade-106">ACE type</span></span></th>
<th><span data-ttu-id="b6ade-107">Struktur</span><span class="sxs-lookup"><span data-stu-id="b6ade-107">Structure</span></span></th>
<th><span data-ttu-id="b6ade-108">ACL-Typ</span><span class="sxs-lookup"><span data-stu-id="b6ade-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-109">Zugriff zulässig</span><span class="sxs-lookup"><span data-stu-id="b6ade-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-111">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-112">Zugriff zulässig</span><span class="sxs-lookup"><span data-stu-id="b6ade-112">Access allowed</span></span></li>
<li><span data-ttu-id="b6ade-113">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-115">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-116">Zugriff zulässig</span><span class="sxs-lookup"><span data-stu-id="b6ade-116">Access allowed</span></span></li>
<li><span data-ttu-id="b6ade-117">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-119">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-120">Zugriff zulässig</span><span class="sxs-lookup"><span data-stu-id="b6ade-120">Access allowed</span></span></li>
<li><span data-ttu-id="b6ade-121">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-121">Object specific</span></span></li>
<li><span data-ttu-id="b6ade-122">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-124">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-125">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b6ade-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-127">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-128">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b6ade-128">Access denied</span></span></li>
<li><span data-ttu-id="b6ade-129">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-131">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-132">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b6ade-132">Access denied</span></span></li>
<li><span data-ttu-id="b6ade-133">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-133">Object specific</span></span></li>
<li><span data-ttu-id="b6ade-134">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-136">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-137">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b6ade-137">Access denied</span></span></li>
<li><span data-ttu-id="b6ade-138">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-140">Räumen</span><span class="sxs-lookup"><span data-stu-id="b6ade-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-141">System Alarm</span><span class="sxs-lookup"><span data-stu-id="b6ade-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-143">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-144">System Alarm</span><span class="sxs-lookup"><span data-stu-id="b6ade-144">System alarm</span></span></li>
<li><span data-ttu-id="b6ade-145">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-147">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-148">System Alarm</span><span class="sxs-lookup"><span data-stu-id="b6ade-148">System alarm</span></span></li>
<li><span data-ttu-id="b6ade-149">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-149">Object specific</span></span></li>
<li><span data-ttu-id="b6ade-150">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-152">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-153">System Alarm</span><span class="sxs-lookup"><span data-stu-id="b6ade-153">System alarm</span></span></li>
<li><span data-ttu-id="b6ade-154">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-156">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-157">System Überwachung</span><span class="sxs-lookup"><span data-stu-id="b6ade-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-159">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-160">System Überwachung</span><span class="sxs-lookup"><span data-stu-id="b6ade-160">System audit</span></span></li>
<li><span data-ttu-id="b6ade-161">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-163">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b6ade-164">System Überwachung</span><span class="sxs-lookup"><span data-stu-id="b6ade-164">System audit</span></span></li>
<li><span data-ttu-id="b6ade-165">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-165">Object specific</span></span></li>
<li><span data-ttu-id="b6ade-166">Ermöglicht den Rückruf während der Zugriffs Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="b6ade-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-168">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b6ade-169">System Überwachung</span><span class="sxs-lookup"><span data-stu-id="b6ade-169">System audit</span></span></li>
<li><span data-ttu-id="b6ade-170">Objekt spezifisch</span><span class="sxs-lookup"><span data-stu-id="b6ade-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="b6ade-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6ade-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="b6ade-172">System</span><span class="sxs-lookup"><span data-stu-id="b6ade-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b6ade-173">System Alarm und objektspezifische System Alarm-ACEs werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6ade-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="b6ade-174">Jeder ACE beginnt mit einer [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="b6ade-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="b6ade-175">Das Format der Daten, die dem Header folgen, variiert je nach dem im Header angegebenen ACE-Typ.</span><span class="sxs-lookup"><span data-stu-id="b6ade-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6ade-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6ade-176">Requirements</span></span>



| <span data-ttu-id="b6ade-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6ade-177">Requirement</span></span> | <span data-ttu-id="b6ade-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ade-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ade-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6ade-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ade-180">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6ade-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b6ade-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6ade-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ade-182">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6ade-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b6ade-183">Header</span><span class="sxs-lookup"><span data-stu-id="b6ade-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ade-184"><dt>WinNT. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6ade-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ade-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ade-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ade-186">**Addace**</span><span class="sxs-lookup"><span data-stu-id="b6ade-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="b6ade-187">**Zugriffs zulässiger \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="b6ade-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="b6ade-188">**Zugriffs \_ Verweigerungs \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="b6ade-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="b6ade-189">**ACL**</span><span class="sxs-lookup"><span data-stu-id="b6ade-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="b6ade-190">**Systemalarm- \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="b6ade-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="b6ade-191">**Systemüberwachungs- \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="b6ade-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

