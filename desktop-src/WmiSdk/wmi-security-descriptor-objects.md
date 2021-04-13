---
description: WMI verfügt über Objekte und Methoden, mit denen Sie Sicherheits Deskriptoren lesen und bearbeiten können, um zu bestimmen, wer Zugriff auf Sicherungs fähige Objekte hat.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: WMI-sicherheitsdeskriptorobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564422"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="4b00c-103">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="4b00c-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="4b00c-104">WMI verfügt über Objekte und Methoden, mit denen Sie Sicherheits Deskriptoren lesen und bearbeiten können, um zu bestimmen, wer Zugriff auf Sicherungs fähige Objekte hat.</span><span class="sxs-lookup"><span data-stu-id="4b00c-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="4b00c-105">Die Rolle der Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4b00c-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="4b00c-106">Access Control und WMI-Sicherheits Objekte</span><span class="sxs-lookup"><span data-stu-id="4b00c-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="4b00c-107">Win32 \_ securityDescriptor-Objekt</span><span class="sxs-lookup"><span data-stu-id="4b00c-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="4b00c-108">DACL und SACL</span><span class="sxs-lookup"><span data-stu-id="4b00c-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="4b00c-109">Win32- \_ ACE, Win32- \_ Treuhänder, Win32- \_ sid</span><span class="sxs-lookup"><span data-stu-id="4b00c-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="4b00c-110">Beispiel: überprüfen, wer Zugriff auf Drucker hat</span><span class="sxs-lookup"><span data-stu-id="4b00c-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="4b00c-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b00c-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="4b00c-112">Die Rolle der Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4b00c-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="4b00c-113">Sicherheits Deskriptoren definieren die Sicherheits Attribute von Sicherungs fähigen Objekten wie Dateien, Registrierungs Schlüsseln, WMI-Namespaces, Druckern, Diensten oder Freigaben.</span><span class="sxs-lookup"><span data-stu-id="4b00c-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="4b00c-114">Eine Sicherheits Beschreibung enthält Informationen zum Besitzer und zur primären Gruppe eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="4b00c-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="4b00c-115">Ein Anbieter kann die Ressourcen Sicherheits Beschreibung mit der Identität eines anfordernden Benutzers vergleichen und ermitteln, ob der Benutzer über die Berechtigung zum Zugriff auf die Ressource verfügt, die ein Benutzer anfordert.</span><span class="sxs-lookup"><span data-stu-id="4b00c-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="4b00c-116">Weitere Informationen finden Sie unter [Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4b00c-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="4b00c-117">Einige WMI-Methoden, wie z. [**b. gezd**](--systemsecurity-getsd.md), geben eine Sicherheits Beschreibung im binären Byte Array Format zurück.</span><span class="sxs-lookup"><span data-stu-id="4b00c-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="4b00c-118">Beginnend mit Windows Vista verwenden Sie die Methoden der [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse, um eine binäre Sicherheits Beschreibung in eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zu konvertieren, die einfacher bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b00c-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="4b00c-119">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4b00c-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="4b00c-120">Access Control und WMI-Sicherheits Objekte</span><span class="sxs-lookup"><span data-stu-id="4b00c-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="4b00c-121">Im folgenden finden Sie eine Liste von WMI-Sicherheits Objekten:</span><span class="sxs-lookup"><span data-stu-id="4b00c-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="4b00c-122">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4b00c-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="4b00c-123">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="4b00c-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="4b00c-124">**Win32- \_ Treuhänder**</span><span class="sxs-lookup"><span data-stu-id="4b00c-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="4b00c-125">**Win32- \_ sid**</span><span class="sxs-lookup"><span data-stu-id="4b00c-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="4b00c-126">Das folgende Diagramm zeigt die Beziehungen zwischen WMI-Sicherheits Objekten.</span><span class="sxs-lookup"><span data-stu-id="4b00c-126">The following diagram shows the relationships among WMI security objects.</span></span>

![Beziehungen zwischen WMI-Sicherheits Objekten](images/security-descriptor.png)

<span data-ttu-id="4b00c-128">Weitere Informationen zur Rolle der Zugriffssicherheit finden Sie unter [Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis), Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md)und [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="4b00c-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="4b00c-129">Win32 \_ securityDescriptor-Objekt</span><span class="sxs-lookup"><span data-stu-id="4b00c-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="4b00c-130">In der folgenden Tabelle sind die Win32-Eigenschaften der [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4b00c-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="4b00c-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4b00c-131">Property</span></span>         | <span data-ttu-id="4b00c-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b00c-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b00c-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="4b00c-133">**ControlFlags**</span></span> | <span data-ttu-id="4b00c-134">Ein Satz von Steuerungs Bits, die die Bedeutung einer SD oder ihrer einzelnen Member qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="4b00c-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="4b00c-135">Weitere Informationen zum Festlegen der **ControlFlags** -Bitwerte finden Sie [**unter \_ Win32 securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="4b00c-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="4b00c-136">**DACL**</span><span class="sxs-lookup"><span data-stu-id="4b00c-136">**DACL**</span></span>         | <span data-ttu-id="4b00c-137">Eine freigegebene [Access Control Liste (ACL)](/windows/desktop/SecAuthZ/access-control-lists) von Benutzern und Gruppen sowie deren Zugriffsrechte für ein gesichertes Objekt.</span><span class="sxs-lookup"><span data-stu-id="4b00c-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="4b00c-138">Diese Eigenschaft enthält ein Array von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanzen, die [Access Control Einträge](/windows/desktop/SecAuthZ/access-control-entries)darstellen.</span><span class="sxs-lookup"><span data-stu-id="4b00c-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="4b00c-139">Weitere Informationen finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="4b00c-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="4b00c-140">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="4b00c-140">**Group**</span></span>        | <span data-ttu-id="4b00c-141">Die Gruppe, zu der dieses gesicherte Objekt gehört.</span><span class="sxs-lookup"><span data-stu-id="4b00c-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="4b00c-142">Diese Eigenschaft enthält eine Instanz des [**Win32- \_ Treuhänders**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , die den Namen, die Domäne und die Sicherheits-ID (SID) der Gruppe enthält, zu der der Besitzer gehört.</span><span class="sxs-lookup"><span data-stu-id="4b00c-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="4b00c-143">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="4b00c-143">**Owner**</span></span>        | <span data-ttu-id="4b00c-144">Besitzer dieses gesicherten Objekts.</span><span class="sxs-lookup"><span data-stu-id="4b00c-144">Owner of this secured object.</span></span> <span data-ttu-id="4b00c-145">Diese Eigenschaft enthält eine Instanz des [Win32- \_ Treuhänders](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , die den Namen, die Domäne und die Sicherheits-ID (SID) des Besitzers enthält.</span><span class="sxs-lookup"><span data-stu-id="4b00c-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="4b00c-146">**SACL**</span><span class="sxs-lookup"><span data-stu-id="4b00c-146">**SACL**</span></span>         | <span data-ttu-id="4b00c-147">Die [System Access Control Liste (ACL)](/windows/desktop/SecAuthZ/access-control-lists) enthält ein Array von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanzen, die den Typ der Zugriffsversuche darstellen, die Überwachungsdaten Sätze für Benutzer oder Gruppen generieren.</span><span class="sxs-lookup"><span data-stu-id="4b00c-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="4b00c-148">Weitere Informationen finden Sie unter [SACL für ein neues Objekt](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="4b00c-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="4b00c-149">DACL und SACL</span><span class="sxs-lookup"><span data-stu-id="4b00c-149">DACL and SACL</span></span>

<span data-ttu-id="4b00c-150">Die Arrays von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekten in der freigegebenen Zugriffs Steuerungs Liste (DACL) und der System Zugriffs Steuerungs Liste {SACL) erstellen eine Verknüpfung zwischen einem Benutzer oder einer Gruppe und Ihren Zugriffsrechten.</span><span class="sxs-lookup"><span data-stu-id="4b00c-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="4b00c-151">Wenn eine DACL-Eigenschaft keinen Zugriffs Steuerungs Eintrag (Access Control Entry, ACE) enthält, werden keine Zugriffsrechte erteilt, und der Zugriff auf das Objekt wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="4b00c-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="4b00c-152">Eine **null** -DACL bietet vollständigen Zugriff auf alle, was ein schwerwiegendes Sicherheitsrisiko darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b00c-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="4b00c-153">Weitere Informationen finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="4b00c-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="4b00c-154">Win32- \_ ACE, Win32- \_ Treuhänder, Win32- \_ sid</span><span class="sxs-lookup"><span data-stu-id="4b00c-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="4b00c-155">Ein [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekt enthält eine Instanz der Win32-Vertrauens nehmer Klasse, die einen Benutzer oder eine Gruppe identifiziert, und eine **AccessMask** -Eigenschaft, bei der es sich um eine Bitmaske handelt, die angibt, welche Aktionen ein Benutzer oder eine Gruppe ausführen kann. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)</span><span class="sxs-lookup"><span data-stu-id="4b00c-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="4b00c-156">Beispielsweise kann einem Benutzer oder einer Gruppe das Recht erteilt werden, eine Datei zu lesen, aber nicht in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4b00c-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="4b00c-157">Ein **Win32- \_ ACE** -Objekt enthält auch einen ACE, der angibt, ob es sich um einen Zulassungs-oder Verweigerungs Zugriff handelt.</span><span class="sxs-lookup"><span data-stu-id="4b00c-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="4b00c-158">Die [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Reihenfolge in einer DACL ist wichtig, da sowohl der Allow-als auch der Deny-Zugriffs Steuerungs Eintrag (ACE) in einer DACL zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4b00c-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="4b00c-159">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="4b00c-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="4b00c-160">Jedes Benutzerkonto oder jede Gruppe, das durch einen [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) repräsentiert wird, verfügt über eine Sicherheits-ID (SID), die ein Konto eindeutig identifiziert, und gibt die Zugriffsrechte des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4b00c-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="4b00c-161">Wie Sie die SID-Daten angeben, hängt vom Betriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="4b00c-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="4b00c-162">Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4b00c-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="4b00c-163">Das folgende Diagramm zeigt den Inhalt einer [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="4b00c-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![Inhalt einer Win32- \- ACE-Instanz](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="4b00c-165">Beispiel: überprüfen, wer Zugriff auf Drucker hat</span><span class="sxs-lookup"><span data-stu-id="4b00c-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="4b00c-166">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Sicherheits Beschreibung des Druckers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b00c-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="4b00c-167">Das Skript ruft die [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) -Methode in der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse auf, um den Deskriptor abzurufen, und bestimmt dann, ob eine freigegebene Access Control Liste (DACL) in der Sicherheits Beschreibung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4b00c-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="4b00c-168">Wenn eine DACL vorhanden ist, erhält das Skript die Liste der Access Control Einträge (ACE) aus der DACL.</span><span class="sxs-lookup"><span data-stu-id="4b00c-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="4b00c-169">Jeder ACE wird durch eine Instanz von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4b00c-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="4b00c-170">Das Skript prüft jeden ACE, um den Namen des Benutzers zu erhalten, und bestimmt, ob der Benutzer Zugriff auf den Drucker hat.</span><span class="sxs-lookup"><span data-stu-id="4b00c-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="4b00c-171">Der Benutzer wird in durch eine Instanz des Win32-Vertrauens nehmers dargestellt, der in die **Win32- \_ ACE** -Instanz eingebettet ist. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)</span><span class="sxs-lookup"><span data-stu-id="4b00c-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="4b00c-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b00c-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b00c-173">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="4b00c-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="4b00c-174">Hilfsklasse für Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4b00c-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="4b00c-175">Bewährte Sicherheitsmethoden</span><span class="sxs-lookup"><span data-stu-id="4b00c-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="4b00c-176">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="4b00c-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="4b00c-177">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="4b00c-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="4b00c-178">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="4b00c-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

