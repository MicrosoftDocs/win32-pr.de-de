---
title: ADSI und Benutzerkontensteuerung
description: Windows und Windows Server verfügen über die Benutzerkontensteuerung, die Auswirkungen auf Anwendungen hat, die Active Directory Service Interfaces (ADSI) verwenden.
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039602"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="f665d-103">ADSI und Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="f665d-103">ADSI and User Account Control</span></span>

<span data-ttu-id="f665d-104">Windows und Windows Server verfügen über die [Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), die Auswirkungen auf Anwendungen hat, die [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f665d-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="f665d-105">Diese Schnittstellen wurden speziell so konzipiert, dass Sie von einem Benutzerkonto mit Administratorrechten auf dem lokalen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f665d-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="f665d-106">**Problem**</span><span class="sxs-lookup"><span data-stu-id="f665d-106">**Problem**</span></span>

<span data-ttu-id="f665d-107">Jedes Mal, wenn eine Anwendung eine Verbindung mit dem Verzeichnis herstellt und versucht, ein ADSI-Objekt zu erstellen, wird das [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) auf Änderungen geprüft.</span><span class="sxs-lookup"><span data-stu-id="f665d-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="f665d-108">Wenn Sie sich seit der letzten Verbindung geändert hat, wird das Schema heruntergeladen und in einem Cache auf dem lokalen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f665d-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="f665d-109">In Windows-Versionen vor Windows Vista war der Standard Speicherort für diesen Cache.</span><span class="sxs-lookup"><span data-stu-id="f665d-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="f665d-110">Anwendungen, die standardmäßig ausgeführt werden (d. h. nicht-Administrator Konten), haben keinen Zugriff auf dieses Verzeichnis. Folglich können Anwendungen, die ADSI-Schnittstellen verwenden, die in diesem Modus ausgeführt werden, das Schema bei jeder Verbindung herunterladen, was sich auf den Durchsatz und die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f665d-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="f665d-111">**Lösungen**</span><span class="sxs-lookup"><span data-stu-id="f665d-111">**Solutions**</span></span>

<span data-ttu-id="f665d-112">*Einzelner Benutzer* : um dieses Problem zu beheben, gibt es neue Registrierungs Steuerungs Schlüssel für ADSI-Anbieter, mit denen die Registrierungs Speicherorte und Dateispeicher Orte für zwischengespeicherte [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Objekte bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="f665d-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="f665d-113">Wenn der Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="f665d-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="f665d-114">wird auf 0 (null) festgelegt, und jeder Benutzer erhält einen anderen Speicherort für ADSI. Registrierungsschlüssel werden in gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f665d-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="f665d-115">und Cache Dateien werden in gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f665d-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="f665d-116">Diese Einstellungen sind die Standardeinstellungen auf Computern, auf denen Windows Server 2008 oder Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f665d-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="f665d-117">*Mehr Benutzer* : Wenn Sie ADSI-Anwendungen auf einem Computer mit vielen Benutzerkonten (z. b. einem Webserver) ausführen, ist es vorzuziehen, nicht viele Kopien des [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Caches zu verwenden, die große Mengen an Speicherplatz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f665d-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="f665d-118">Festlegen des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="f665d-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="f665d-119">auf 1 (eins) wird ADSI auf das vorherige Verhalten zurückgesetzt. alle [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Objekte werden an Ihren vorherigen Speicherorten gespeichert. der Registrierungsschlüssel wird in</span><span class="sxs-lookup"><span data-stu-id="f665d-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="f665d-120">die Cachedatei wird in</span><span class="sxs-lookup"><span data-stu-id="f665d-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="f665d-121">In diesem Fall sollte die Anwendung von Administrator Konten ausgeführt werden. Dadurch wird die Schema Datei im globalen Speicherort für die zukünftige Verwendung durch die Benutzer mit weniger Berechtigungen zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="f665d-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 