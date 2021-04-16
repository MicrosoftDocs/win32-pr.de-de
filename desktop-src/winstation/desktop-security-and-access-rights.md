---
title: Desktop Sicherheit und Zugriffsrechte
description: Sicherheit ermöglicht es Ihnen, den Zugriff auf Desktop Objekte zu steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Modell.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390639"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="c5d5e-104">Desktop Sicherheit und Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="c5d5e-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="c5d5e-105">Sicherheit ermöglicht es Ihnen, den Zugriff auf Desktop Objekte zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="c5d5e-106">Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="c5d5e-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="c5d5e-107">Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für ein Desktop Objekt angeben, wenn Sie die Funktion "up [**Desktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) " oder " [**kreatedesktopex**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="c5d5e-108">Wenn Sie NULL angeben, erhält der Desktop eine Standard Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="c5d5e-109">Die ACLs in der Standard Sicherheits Beschreibung für einen Desktop stammen aus der übergeordneten Fenster Station.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="c5d5e-110">Zum Abrufen oder Festlegen der Sicherheits Beschreibung eines Fenster Stations Objekts aufrufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="c5d5e-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="c5d5e-111">Wenn Sie die Funktion [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) oder [**openinputdesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="c5d5e-112">Zu den gültigen Zugriffsrechten für Desktop Objekte gehören die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="c5d5e-113">In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="c5d5e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d5e-114">Value</span></span>                       | <span data-ttu-id="c5d5e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5d5e-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d5e-116">Delete (0x00010000l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="c5d5e-117">Erforderlich, um das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c5d5e-118">Read- \_ Steuerelement (0x00020000l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="c5d5e-119">Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="c5d5e-120">Um die SACL zu lesen oder zu schreiben, müssen Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht anfordern.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="c5d5e-121">Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="c5d5e-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="c5d5e-122">Synchronisieren (0x00100000l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="c5d5e-123">Wird für Desktop Objekte nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c5d5e-124">\_DAC schreiben (0x00040000l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="c5d5e-125">Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="c5d5e-126">Schreib \_ Besitzer (0x00080000l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="c5d5e-127">Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="c5d5e-128">In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="c5d5e-129">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="c5d5e-129">Access right</span></span>                       | <span data-ttu-id="c5d5e-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5d5e-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d5e-131">Desktop " \_ beatemdeu" (0x0004l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="c5d5e-132">Erforderlich, um auf dem Desktop ein Menü zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="c5d5e-133">Desktop- \_ kreatewindow (0x0002l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="c5d5e-134">Erforderlich, um auf dem Desktop ein Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="c5d5e-135">Desktop \_ Aufzählung (0x0040l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="c5d5e-136">Erforderlich, damit der Desktop aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="c5d5e-137">Desktop- \_ Hostingsteuerelement (0x0008l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="c5d5e-138">Erforderlich, um einen der Fenster Hooks einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="c5d5e-139">Desktop \_ journalplayback (0x0020l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="c5d5e-140">Erforderlich, um die Journal Wiedergabe auf einem Desktop auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="c5d5e-141">Desktop \_ journalrecord (0x0010l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="c5d5e-142">Erforderlich, um die Journal Aufzeichnung auf einem Desktop auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="c5d5e-143">Desktop-Schreib \_ Objekte (0x0001l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="c5d5e-144">Erforderlich zum Lesen von Objekten auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="c5d5e-145">Desktop \_ switchdesktop (0x0100l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="c5d5e-146">Erforderlich, um den Desktop mithilfe der [**switchdesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) -Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="c5d5e-147">Desktop-Schreib \_ Objekte (0x0080l)</span><span class="sxs-lookup"><span data-stu-id="c5d5e-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="c5d5e-148">Erforderlich zum Schreiben von Objekten auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="c5d5e-149">Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für ein Desktop Objekt, das in der interaktiven Fenster Station der Anmelde Sitzung des Benutzers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c5d5e-150">Zugriffsrecht</span><span class="sxs-lookup"><span data-stu-id="c5d5e-150">Access right</span></span></th>
<th><span data-ttu-id="c5d5e-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5d5e-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5d5e-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="c5d5e-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="c5d5e-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="c5d5e-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c5d5e-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="c5d5e-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="c5d5e-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5d5e-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="c5d5e-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="c5d5e-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="c5d5e-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="c5d5e-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="c5d5e-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="c5d5e-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="c5d5e-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="c5d5e-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="c5d5e-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="c5d5e-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="c5d5e-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c5d5e-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="c5d5e-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5d5e-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="c5d5e-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="c5d5e-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="c5d5e-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5d5e-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="c5d5e-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="c5d5e-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="c5d5e-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="c5d5e-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="c5d5e-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="c5d5e-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="c5d5e-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="c5d5e-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="c5d5e-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="c5d5e-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="c5d5e-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="c5d5e-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="c5d5e-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="c5d5e-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c5d5e-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="c5d5e-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="c5d5e-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="c5d5e-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c5d5e-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="c5d5e-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c5d5e-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c5d5e-178">Sie können das Zugriffs \_ System \_ -Sicherheits Zugriffsrecht für ein Desktop Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="c5d5e-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="c5d5e-179">Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="c5d5e-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 