---
title: Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte
description: Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (zwischen Benutzern), Lese-/Schreibzugriff.
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218919"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="b472d-103">Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte</span><span class="sxs-lookup"><span data-stu-id="b472d-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="b472d-104">Standardmäßig gewähren sowohl Windows Vista als auch Windows Server 2008 Administratoren und Benutzern, die direkt auf dem Computer angemeldet sind (zwischen Benutzern), Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b472d-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="b472d-105">In Windows XP und Windows Server 2003 muss ein Administrator diesen Geräten jedoch Lese-/Schreibberechtigungen für andere Benutzergruppen erteilen.</span><span class="sxs-lookup"><span data-stu-id="b472d-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="b472d-106">Ein Administrator kann bestimmte gerätebezogene Berechtigungen für Poweruser und interaktive Benutzer anpassen.</span><span class="sxs-lookup"><span data-stu-id="b472d-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="b472d-107">Um den entsprechenden Bereich für Gruppenberechtigungen in Windows XP zu erreichen, klicken Sie auf **Start**, klicken Sie auf **Ausführen**, geben Sie **gpeer dit. msc** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b472d-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="b472d-108">Erweitern Sie in der Gruppenrichtlinie-Schnittstelle **Computer Konfiguration**, erweitern Sie **Windows-Einstellungen**, erweitern Sie **Sicherheitseinstellungen**, erweitern Sie **lokale Richtlinien**, und doppelklicken Sie auf **Sicherheitsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="b472d-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Screenshot, der das Fenster "Gruppenrichtlinie" mit einer Richtlinie anzeigt, die im Bereich "Richtlinie" ausgewählt ist.](images/gpolpanel.jpg)

<span data-ttu-id="b472d-110">In diesem Bereich muss ein Administrator die Einstellungen der beiden Geräteoptionen angeben, um die erforderlichen Gruppenberechtigungen bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="b472d-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="b472d-111">Legen Sie "Geräte: Beschränken des CD-ROM-Zugriffs auf lokal angemeldete Benutzer" auf " **aktiviert** " fest.</span><span class="sxs-lookup"><span data-stu-id="b472d-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="b472d-112">Legen Sie für **Administratoren und Hauptbenutzer** den Wert "Geräte: erlaubt zum Formatieren und Auswerfen von Wechselmedien" fest.</span><span class="sxs-lookup"><span data-stu-id="b472d-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="b472d-113">Es ist auch möglich, Windows Vista-Berechtigungen zu emulieren, indem Sie diese Option auf **Administratoren und interaktive Benutzer** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b472d-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="b472d-114">Obwohl eine bestimmte Benutzeroberfläche in Windows XP oder Windows Server 2003 für die Verwendung von [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) oder [setupdisetdeviceregistryproperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)nicht vorhanden ist, können diese APIs verwendet werden, um benutzerdefinierten Benutzergruppen Geräte Berechtigungen zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="b472d-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="b472d-115">Beispielsweise wird durch einen Aufrufen von **setsecurityinfo** Berechtigungen für Benutzergruppen erteilt.</span><span class="sxs-lookup"><span data-stu-id="b472d-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="b472d-116">Berechtigungs Änderungen mit dieser API sind temporär und werden nicht über einen Neustart hinweg beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b472d-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="b472d-117">Durch Aufrufen von [setupdisetdeviceregistryproperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) werden jedoch die Berechtigungs Änderungen in der Registrierung implementiert, die bei einem Neustart beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="b472d-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b472d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b472d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b472d-119">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="b472d-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="b472d-120">**Setsecurityinfo**</span><span class="sxs-lookup"><span data-stu-id="b472d-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="b472d-121">Setupdisetdeviceregistryproperty</span><span class="sxs-lookup"><span data-stu-id="b472d-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 