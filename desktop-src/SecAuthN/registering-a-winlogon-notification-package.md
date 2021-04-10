---
description: Informationen zu Winlogon-Benachrichtigungs Paketen werden in der Registrierung gespeichert. Registrierungseinträge geben den Namen des Benachrichtigungs Pakets, den Namen der dll, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse verarbeiten.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrieren eines Winlogon-Benachrichtigungs Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215880"
---
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="dea8f-104">Registrieren eines Winlogon-Benachrichtigungs Pakets</span><span class="sxs-lookup"><span data-stu-id="dea8f-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="dea8f-105">Informationen zu [*Winlogon*](../secgloss/w-gly.md) -Benachrichtigungs Paketen werden in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dea8f-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="dea8f-106">Registrierungseinträge geben den Namen des Benachrichtigungs Pakets, den Namen der dll, die das Paket implementiert, und die Namen der Funktionen an, die Winlogon-Ereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dea8f-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="dea8f-107">Wenn Winlogon gestartet wird, wird die Registrierung überprüft und alle registrierten Benachrichtigungs Pakete geladen.</span><span class="sxs-lookup"><span data-stu-id="dea8f-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="dea8f-108">Wenn ein Ereignis auftritt, ruft Winlogon die festgelegte Ereignishandlerfunktion für jedes Paket auf.</span><span class="sxs-lookup"><span data-stu-id="dea8f-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="dea8f-109">Mehrere Ereignis Benachrichtigungs Pakete können auf einem System registriert werden.</span><span class="sxs-lookup"><span data-stu-id="dea8f-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="dea8f-110">Erstellen Sie zum Registrieren des Benachrichtigungs Pakets einen Registrierungsschlüssel mit dem Namen **Benachrichtigen** als Unterschlüssel des folgenden Registrierungsschlüssels, und fügen Sie die in den [Registrierungs Einträgen](registry-entries.md)beschriebenen Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="dea8f-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="dea8f-111">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="dea8f-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
