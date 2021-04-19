---
description: Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administrator Konto ausgeführt werden, können eine Namespace-Sicherheits Beschreibung ändern.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Festlegen von Namespace-Sicherheits Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353972"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="328e5-103">Festlegen von Namespace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="328e5-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="328e5-104">Sowohl C++-Anwendungen als auch Skripts, die unter einem vollständigen Administrator Konto ausgeführt werden, können eine Namespace-Sicherheits Beschreibung ändern.</span><span class="sxs-lookup"><span data-stu-id="328e5-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="328e5-105">Namespace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="328e5-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="328e5-106">Jeder WMI-Namespace verfügt über eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly), die es jedem Namespace ermöglicht, eindeutige Sicherheitseinstellungen festzulegen, die festlegen, wer Zugriff auf die Namespace Daten und-Methoden hat.</span><span class="sxs-lookup"><span data-stu-id="328e5-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="328e5-107">Weitere Informationen zur WMI-Zugriffssicherheit finden [Sie unter Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="328e5-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="328e5-108">Der [Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md) beschreibt die Standard Sicherheitseinstellungen für WMI-Namespaces und die Sicherheitsüberwachung in WMI.</span><span class="sxs-lookup"><span data-stu-id="328e5-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="328e5-109">Sie können die Konto Berechtigungen für jeden WMI-Namespace im WMI-Repository (CIM) auf folgende Weise festlegen:</span><span class="sxs-lookup"><span data-stu-id="328e5-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="328e5-110">Wenn der Namespace in der MOF-Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="328e5-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="328e5-111">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="328e5-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="328e5-112">Manuell mit dem WMI-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="328e5-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="328e5-113">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="328e5-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="328e5-114">Programm gesteuert durch Aufrufen der Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="328e5-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="328e5-115">Die folgenden Methoden des [**\_ \_ SystemSecurity**](--systemsecurity.md) -Objekts, das mit jedem Namespace verknüpft ist, ermöglichen es Ihnen, die Sicherheit für einen Namespace zu lesen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="328e5-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="328e5-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**Getcalleraccessrights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-117">Legt den *Rights* -Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.</span><span class="sxs-lookup"><span data-stu-id="328e5-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="328e5-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-119">Ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="328e5-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="328e5-120">Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="328e5-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="328e5-121">Wenn Sie ein Skript schreiben, verwenden Sie die [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="328e5-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="328e5-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-123">Legt die Sicherheits Beschreibung für den Namespace fest, mit dem ein Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="328e5-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="328e5-124">Diese Methode erfordert eine Sicherheits Beschreibung im Format des binären Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="328e5-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="328e5-125">Wenn Sie ein Skript schreiben, verwenden Sie die [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="328e5-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="328e5-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-127">Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, der der-Instanz von [**\_ \_ SystemSecurity**](--systemsecurity.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="328e5-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="328e5-128">Die Sicherheits Beschreibung wird als Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="328e5-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="328e5-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-130">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="328e5-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="328e5-131">Die Sicherheits Beschreibung wird durch eine Instanz von [**\_ \_ securityDescriptor**](--securitydescriptor.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="328e5-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="328e5-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-133">Ruft die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern ab, auf denen veraltete Versionen von Windows ausgeführt werden, bei denen die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="328e5-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="328e5-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="328e5-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="328e5-135">Legt die Remote Zugriffsrechte für eine Liste einzelner Benutzer auf Computern fest, auf denen veraltete Versionen von Windows ausgeführt werden, wobei die Zugriffs Steuerung durch Windows-Sicherheits Deskriptoren nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="328e5-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="328e5-136">Wenn Sie Skripts schreiben, verwenden Sie " [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) " und " [**SETSECURITYDESCRIPTOR**](setsecuritydescriptor-method-in-class---systemsecurity.md)".</span><span class="sxs-lookup"><span data-stu-id="328e5-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="328e5-137">Sie können die-Methoden der [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse verwenden, um die Sicherheits Deskriptoren zu ändern.</span><span class="sxs-lookup"><span data-stu-id="328e5-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="328e5-138">Wenn Sie in C++ programmieren, können Sie die binäre Sicherheits Beschreibung mithilfe von [SDDL (Security Deskriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="328e5-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="328e5-139">Beachten Sie, dass sich die [Benutzerkontensteuerung (User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) , UAC) ab Windows Vista auf den Zugriff auf WMI-Daten auswirkt und was mit dem [*WMI-Steuer*](gloss-w.md)Element konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="328e5-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="328e5-140">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="328e5-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="328e5-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="328e5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="328e5-142">Sichern von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="328e5-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="328e5-143">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="328e5-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="328e5-144">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="328e5-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="328e5-145">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="328e5-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
