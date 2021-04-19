---
title: Sicherheit und Zugriffsrechte für die Fenster Station
description: Mithilfe der Sicherheit können Sie den Zugriff auf Fenster Station-Objekte steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Modell.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341524"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="4220c-104">Sicherheit und Zugriffsrechte für die Fenster Station</span><span class="sxs-lookup"><span data-stu-id="4220c-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="4220c-105">Mithilfe der Sicherheit können Sie den Zugriff auf Fenster Station-Objekte steuern.</span><span class="sxs-lookup"><span data-stu-id="4220c-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="4220c-106">Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="4220c-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="4220c-107">Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für ein Fenster Station-Objekt angeben, wenn [**Sie die Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) "Funktion in der Funktion" aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="4220c-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="4220c-108">Wenn Sie NULL angeben, erhält die Fenster Station eine Standard Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4220c-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="4220c-109">Die ACLs in der Standard Sicherheits Beschreibung für eine Fenster Station stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.</span><span class="sxs-lookup"><span data-stu-id="4220c-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="4220c-110">Zum Abrufen oder Festlegen der Sicherheits Beschreibung eines Fenster Stations Objekts aufrufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="4220c-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="4220c-111">Wenn Sie die [**openwindowstation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) -Funktion aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4220c-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="4220c-112">Zu den gültigen Zugriffsrechten für Fenster Stations Objekte gehören die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="4220c-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="4220c-113">In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4220c-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="4220c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4220c-114">Value</span></span>                       | <span data-ttu-id="4220c-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4220c-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4220c-116">Delete (0x00010000l)</span><span class="sxs-lookup"><span data-stu-id="4220c-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="4220c-117">Erforderlich, um das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4220c-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4220c-118">Read- \_ Steuerelement (0x00020000l)</span><span class="sxs-lookup"><span data-stu-id="4220c-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="4220c-119">Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen.</span><span class="sxs-lookup"><span data-stu-id="4220c-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="4220c-120">Um die SACL zu lesen oder zu schreiben, müssen Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht anfordern.</span><span class="sxs-lookup"><span data-stu-id="4220c-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="4220c-121">Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="4220c-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="4220c-122">Synchronisieren (0x00100000l)</span><span class="sxs-lookup"><span data-stu-id="4220c-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="4220c-123">Wird für Fenster Station-Objekte nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4220c-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="4220c-124">\_DAC schreiben (0x00040000l)</span><span class="sxs-lookup"><span data-stu-id="4220c-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="4220c-125">Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4220c-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="4220c-126">Schreib \_ Besitzer (0x00080000l)</span><span class="sxs-lookup"><span data-stu-id="4220c-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="4220c-127">Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4220c-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="4220c-128">In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4220c-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="4220c-129">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="4220c-129">Access right</span></span>                        | <span data-ttu-id="4220c-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4220c-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4220c-131">Winsta \_ All- \_ Zugriff (0x37f)</span><span class="sxs-lookup"><span data-stu-id="4220c-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="4220c-132">Alle möglichen Zugriffsrechte für die Fenster Station.</span><span class="sxs-lookup"><span data-stu-id="4220c-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="4220c-133">Winsta \_ accessclipboard (0x0004l)</span><span class="sxs-lookup"><span data-stu-id="4220c-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="4220c-134">Erforderlich, um die Zwischenablage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4220c-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="4220c-135">Winsta \_ accessglobalatome (0x0020l)</span><span class="sxs-lookup"><span data-stu-id="4220c-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="4220c-136">Erforderlich, um globale Atome zu manipulieren.</span><span class="sxs-lookup"><span data-stu-id="4220c-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4220c-137">Winsta \_ -kreatedesktop (0x0008l)</span><span class="sxs-lookup"><span data-stu-id="4220c-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="4220c-138">Erforderlich, um neue Desktop Objekte auf der Fenster Station zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4220c-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="4220c-139">Winsta- \_ EnumDesktops (0x0001l)</span><span class="sxs-lookup"><span data-stu-id="4220c-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="4220c-140">Zum Auflisten vorhandener Desktop Objekte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4220c-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="4220c-141">Winsta- \_ Enumeration (0x0100l)</span><span class="sxs-lookup"><span data-stu-id="4220c-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="4220c-142">Erforderlich, damit die Fenster Station aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="4220c-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="4220c-143">Winsta- \_ exitwindows (0x0040l)</span><span class="sxs-lookup"><span data-stu-id="4220c-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="4220c-144">Erforderlich, um die [**exitwindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) -oder [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgreich aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4220c-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="4220c-145">Fenster Stationen können von Benutzern gemeinsam genutzt werden. mit diesem Zugriffstyp kann verhindert werden, dass andere Benutzer einer Fenster Station sich vom Besitzer der Fenster Station abmelden.</span><span class="sxs-lookup"><span data-stu-id="4220c-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="4220c-146">Winsta-Read- \_ Attribute (0x0002l)</span><span class="sxs-lookup"><span data-stu-id="4220c-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="4220c-147">Erforderlich, um die Attribute eines Fenster Station-Objekts zu lesen.</span><span class="sxs-lookup"><span data-stu-id="4220c-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="4220c-148">Dieses Attribut schließt Farbeinstellungen und andere Eigenschaften der globalen Fenster Station ein.</span><span class="sxs-lookup"><span data-stu-id="4220c-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="4220c-149">Winsta- \_ Bildschirm (0x0200l)</span><span class="sxs-lookup"><span data-stu-id="4220c-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="4220c-150">Für den Zugriff auf Bildschirminhalte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4220c-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="4220c-151">Winsta- \_ Beschreib teattribute (0x0010l)</span><span class="sxs-lookup"><span data-stu-id="4220c-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="4220c-152">Erforderlich, um die Attribute eines Fenster Station-Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4220c-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="4220c-153">Zu den Attributen zählen Farbeinstellungen und andere Eigenschaften der globalen Fenster Station.</span><span class="sxs-lookup"><span data-stu-id="4220c-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="4220c-154">Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für das interaktive Fenster Station-Objekt, bei dem es sich um die der Anmelde Sitzung des interaktiven Benutzers zugewiesene Fenster Station handelt.</span><span class="sxs-lookup"><span data-stu-id="4220c-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4220c-155">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="4220c-155">Access right</span></span></th>
<th><span data-ttu-id="4220c-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4220c-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4220c-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="4220c-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="4220c-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="4220c-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="4220c-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4220c-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4220c-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4220c-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4220c-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="4220c-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="4220c-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4220c-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="4220c-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="4220c-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="4220c-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="4220c-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4220c-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4220c-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4220c-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4220c-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4220c-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4220c-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="4220c-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4220c-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="4220c-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4220c-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4220c-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4220c-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4220c-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="4220c-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="4220c-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="4220c-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="4220c-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4220c-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4220c-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4220c-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4220c-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4220c-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4220c-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4220c-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4220c-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4220c-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4220c-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4220c-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="4220c-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="4220c-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="4220c-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="4220c-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4220c-183">Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für ein nicht interaktives Fenster Station-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4220c-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="4220c-184">Das System weist nicht interaktive Fenster Stationen allen anderen Anmelde Sitzungen als der des interaktiven Benutzers zu.</span><span class="sxs-lookup"><span data-stu-id="4220c-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4220c-185">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="4220c-185">Access right</span></span></th>
<th><span data-ttu-id="4220c-186">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4220c-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4220c-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="4220c-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="4220c-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="4220c-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="4220c-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4220c-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4220c-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4220c-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4220c-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4220c-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="4220c-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="4220c-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="4220c-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="4220c-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4220c-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4220c-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4220c-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4220c-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4220c-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="4220c-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="4220c-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="4220c-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4220c-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4220c-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4220c-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4220c-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="4220c-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="4220c-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="4220c-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="4220c-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="4220c-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="4220c-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="4220c-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="4220c-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="4220c-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="4220c-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="4220c-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="4220c-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4220c-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="4220c-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="4220c-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="4220c-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="4220c-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4220c-209">Sie können das Zugriffs \_ System \_ -Sicherheits Zugriffsrecht auf ein Fenster Station-Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="4220c-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="4220c-210">Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="4220c-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 