---
title: Erstellen eines Remotedesktopprotokoll Anbieters
description: Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters. Der Protokoll-Manager wird als com-Server implementiert und an einem Speicherort registriert, der beim Starten des Remotedesktopdienste Dienstanbieter durchsucht wird.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338558"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="dcfaf-104">Erstellen eines Remotedesktopprotokoll Anbieters</span><span class="sxs-lookup"><span data-stu-id="dcfaf-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="dcfaf-105">Die folgenden Abschnitte enthalten Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters.</span><span class="sxs-lookup"><span data-stu-id="dcfaf-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="dcfaf-106">Der Protokoll-Manager wird als com-Server implementiert und an einem Speicherort registriert, der beim Starten des Remotedesktopdienste Dienstanbieter durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="dcfaf-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dcfaf-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dcfaf-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="dcfaf-108">Registrieren des Protokoll-Managers</span><span class="sxs-lookup"><span data-stu-id="dcfaf-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="dcfaf-109">Sie müssen mindestens einen Registrierungs Wert Eintrag für den Protokoll-Manager erstellen, damit der Remotedesktopdienste Dienst ihn instanziieren kann.</span><span class="sxs-lookup"><span data-stu-id="dcfaf-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="dcfaf-110">Methoden aufrufssequenz</span><span class="sxs-lookup"><span data-stu-id="dcfaf-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="dcfaf-111">Der Remotedesktopdienste-Dienst und Ihr Protokoll Anbieter werden einander in klar definierten Sequenzen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dcfaf-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="dcfaf-112">Registrieren des Protokoll-Managers</span><span class="sxs-lookup"><span data-stu-id="dcfaf-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="dcfaf-113">Methoden aufrufssequenz</span><span class="sxs-lookup"><span data-stu-id="dcfaf-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="dcfaf-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dcfaf-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcfaf-115">Remotedesktopprotokoll Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="dcfaf-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="dcfaf-116">Verwenden von Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="dcfaf-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




