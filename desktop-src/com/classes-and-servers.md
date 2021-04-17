---
title: Klassen und Server
description: Klassen und Server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391067"
---
# <a name="classes-and-servers"></a><span data-ttu-id="e00db-103">Klassen und Server</span><span class="sxs-lookup"><span data-stu-id="e00db-103">Classes and Servers</span></span>

<span data-ttu-id="e00db-104">COM verwendet **HKEY \_ - \_ Klassen** für Computer weite Einstellungen, bietet aber auch eine benutzerspezifische Konfiguration von CLSIDs, um Sicherheit und Flexibilität zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="e00db-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="e00db-105">COM prüft zuerst **HKEY- \_ \_ \\ Software \\ Klassen für aktuelle Benutzer** , bevor Sie unter **HKEY \_ Classes \_ root** suchen.</span><span class="sxs-lookup"><span data-stu-id="e00db-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="e00db-106">COM behält Computer weite Informationen im Zusammenhang mit CLSIDs unter **HKEY \_ Classes \_ root \\ CLSID** bei und speichert benutzerspezifische Klassen Informationen unter **HKEY \_ Current \_ User \\ Software \\ Classes \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="e00db-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="e00db-107">COM-Server unterstützen die Selbstregistrierung.</span><span class="sxs-lookup"><span data-stu-id="e00db-107">COM servers support self-registration.</span></span> <span data-ttu-id="e00db-108">Bei einem in-Process-Server bedeutet dies, dass die dll die folgenden Funktionen exportieren muss:</span><span class="sxs-lookup"><span data-stu-id="e00db-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="e00db-109">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="e00db-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="e00db-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="e00db-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="e00db-111">Sie müssen diese Funktionen mithilfe einer Modul Definitionsdatei, Linker Switches oder Compilerdirektiven explizit exportieren.</span><span class="sxs-lookup"><span data-stu-id="e00db-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="e00db-112">Der Klassen Speicher verwendet diese Funktionen, um die lokale Registrierung zu konfigurieren, nachdem die Datei auf den Client Computer heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="e00db-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="e00db-113">Zusätzlich zum Klassen Speicher werden diese Funktionen auch von anderen Umgebungen verwendet, um Server auf Host Computern zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e00db-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e00db-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e00db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e00db-115">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e00db-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 