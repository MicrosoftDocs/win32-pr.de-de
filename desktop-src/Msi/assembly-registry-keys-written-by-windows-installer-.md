---
description: Wenn Assemblys von einem Windows Installer Paket installiert oder angekündigt werden, speichert das Installationsprogramm Informationen zu diesen Assemblys in der Registrierung des lokalen Systems.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Von Windows Installer geschriebene assemblyregistrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528868"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="57ca1-103">Von Windows Installer geschriebene assemblyregistrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="57ca1-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="57ca1-104">Wenn Assemblys von einem Windows Installer Paket installiert oder angekündigt werden, speichert das Installationsprogramm Informationen zu diesen Assemblys in der Registrierung des lokalen Systems.</span><span class="sxs-lookup"><span data-stu-id="57ca1-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="57ca1-105">Beachten Sie, dass diese Registrierungsschlüssel nur für die interne Verwendung durch Windows Installer vorgesehen sind und nicht von Ihrer Anwendung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57ca1-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="57ca1-106">Der Inhalt, der Speicherort und die Struktur der in diesen Schlüsseln gespeicherten Informationen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="57ca1-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="57ca1-107">Anwendungen sollten sich zum Verwalten von Assemblys auf [**msiprovidebug**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) verlassen.</span><span class="sxs-lookup"><span data-stu-id="57ca1-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="57ca1-108">Assemblys werden durch ihre Assemblynamen registriert.</span><span class="sxs-lookup"><span data-stu-id="57ca1-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="57ca1-109">Die Namen der Werte, die an den folgenden Speicherorten gespeichert sind, sind die Assemblynamen.</span><span class="sxs-lookup"><span data-stu-id="57ca1-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="57ca1-110">Die tatsächlichen Werte sind vom Typ reg \_ \_ MultiSZ und enthalten Daten, die von [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) zum Installieren oder Reparieren von Assemblys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57ca1-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="57ca1-111">Informationen zu privaten Assemblys</span><span class="sxs-lookup"><span data-stu-id="57ca1-111">Information About Private Assemblies</span></span>

<span data-ttu-id="57ca1-112">Windows Installer speichert Informationen zu privaten Assemblys, die von Windows Installer Paketen übertragen wurden, die als verwaltete Anwendungen pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="57ca1-113">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Installer** \\ **Verwaltet** \\ **_Benutzer-SID_ *_\\_*** Installationsassemblypfad \\  \\ \* *_zur Konfigurationsdatei_* _</span><span class="sxs-lookup"><span data-stu-id="57ca1-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="57ca1-114">Windows Installer speichert Informationen zu privaten Assemblys, die von Windows Installer Paketen getragen werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="57ca1-115">_*HKCU- **\\** Software **\\** Microsoft Installer- **\\** Assemblypfad **\\** **\\** _zur Konfigurationsdatei_*_</span><span class="sxs-lookup"><span data-stu-id="57ca1-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="57ca1-116">In Windows Installer werden Informationen zu privaten Assemblys gespeichert, die von Windows Installer Paketen übertragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="57ca1-117">_*Assemblypfad der HKLM- **\\** Software **\\** Klassen **\\** Installations **\\** **\\** _Pfad zur Konfigurationsdatei_*_</span><span class="sxs-lookup"><span data-stu-id="57ca1-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="57ca1-118">Informationen zu globalen oder freigegebenen Assemblys</span><span class="sxs-lookup"><span data-stu-id="57ca1-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="57ca1-119">In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen verwendet werden, die als verwaltete Anwendungen pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="57ca1-120">_*HKLM **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User sid_*_ \\ _ *installationsassemblys **\\** **\\** Global*\*</span><span class="sxs-lookup"><span data-stu-id="57ca1-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="57ca1-121">In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen verwendet werden, die pro Benutzer unter dem folgenden Registrierungsschlüssel installiert wurden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="57ca1-122">**HKCU** \\ **Software** \\ **Microsoft** \\ **Installer** \\ Assemblys  \\ **Global**</span><span class="sxs-lookup"><span data-stu-id="57ca1-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="57ca1-123">In Windows Installer werden Informationen zu freigegebenen Assemblys gespeichert, die von Windows Installer Paketen getragen und pro Computer unter dem folgenden Registrierungsschlüssel installiert werden:</span><span class="sxs-lookup"><span data-stu-id="57ca1-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="57ca1-124">**HKLM** \\ **Software** \\ **Klassen** \\ **Installer** \\ Assemblys  \\ **Global**</span><span class="sxs-lookup"><span data-stu-id="57ca1-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



