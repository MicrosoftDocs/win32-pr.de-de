---
title: Client Registrierung des virtuellen Kanals
description: Der Name der Client-DLL muss in der Registrierung gespeichert werden.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727896"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="3a3e0-103">Client Registrierung des virtuellen Kanals</span><span class="sxs-lookup"><span data-stu-id="3a3e0-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="3a3e0-104">Der Name der Client-DLL muss in der Registrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="3a3e0-105">Fügen Sie in der Registrierung einen Unterschlüssel zu einem der folgenden Speicherorte hinzu:</span><span class="sxs-lookup"><span data-stu-id="3a3e0-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="3a3e0-106">**HKEY \_ Aktuelle \_** \\ **Software Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Standard**- \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="3a3e0-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="3a3e0-107">**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Connection** \\  -Add-ins</span><span class="sxs-lookup"><span data-stu-id="3a3e0-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="3a3e0-108">Im Registrierungs Pfad stellt *Connection* den Namen einer Verbindung im Verbindungs-Manager dar.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="3a3e0-109">Einträge unter dem **\\ Standardschlüssel \\ AddIns** gelten für alle Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="3a3e0-110">Einträge unter dem Schlüssel für die **\\ ***Verbindungs***- \\ AddIns** gelten nur für die durch die *Verbindung* identifizierte Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="3a3e0-111">Verbindungen können mithilfe des Verbindungs-Managers erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="3a3e0-112">Dem Unterschlüssel kann ein beliebiger Name zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-112">The subkey can be given any name.</span></span> <span data-ttu-id="3a3e0-113">Er muss einen **reg \_ SZ** -oder **reg \_ Expand \_** -Wert enthalten, der optional einen **reg \_ DWORD** -Wert enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="3a3e0-114">Die Syntax des " **reg \_ SZ** "-oder " **reg \_ Expand \_** "-Werts lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="3a3e0-115">Wenn " **Name** " ein reg-Wert "reg" ist, kann er nicht erweiterte Umgebungsvariablen enthalten, die zur Laufzeit erweitert werden. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="3a3e0-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="3a3e0-116">Der Wert von " *dllName* " kann ein voll qualifizierter Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="3a3e0-117">Wenn *dllName* keinen Pfad enthält, wird die Standard-dll-Suchstrategie verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="3a3e0-118">Weitere Informationen finden Sie im Abschnitt "Hinweise" für [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="3a3e0-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 