---
title: Verwenden von TSB
description: Jeder an die TSB gesendete Befehl ist einer bestimmten Entität zugeordnet. Dies wird erreicht, indem ein oder mehrere Kontexte für eine Entität erstellt werden, die dann jedem nachfolgenden von dieser Entität übermittelten Befehl zugeordnet werden.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TDie Basisdienste für TPM, Beispiele
- Basisdienste-TSB von TPM mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947765"
---
# <a name="using-tbs"></a><span data-ttu-id="23db7-106">Verwenden von TSB</span><span class="sxs-lookup"><span data-stu-id="23db7-106">Using TBS</span></span>

<span data-ttu-id="23db7-107">Die TPM-Basisdienste-Funktion ist in vier Funktionsbereiche unterteilt:</span><span class="sxs-lookup"><span data-stu-id="23db7-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="23db7-108">Ressourcenvirtualisierung</span><span class="sxs-lookup"><span data-stu-id="23db7-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="23db7-109">Befehls Planung</span><span class="sxs-lookup"><span data-stu-id="23db7-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="23db7-110">Energieverwaltung</span><span class="sxs-lookup"><span data-stu-id="23db7-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="23db7-111">Befehls Blockierung</span><span class="sxs-lookup"><span data-stu-id="23db7-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="23db7-112">Um sicherzustellen, dass verschiedene Entitäten nicht auf die Ressourcen der anderen zugreifen können, wird jeder an den TSB gesendete Befehl einer bestimmten Entität zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="23db7-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="23db7-113">Dies wird erreicht, indem ein oder mehrere Kontexte für eine Entität erstellt werden, die dann jedem nachfolgenden von dieser Entität übermittelten Befehl zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="23db7-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="23db7-114">Jeder Befehl enthält ein Kontext Objekt, das es TSB ermöglicht, TPM-Befehle im entsprechenden Kontext auszuführen.</span><span class="sxs-lookup"><span data-stu-id="23db7-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="23db7-115">Alle durch Befehle erstellten Objekte werden vom TPM geleert, wenn der Kontext geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="23db7-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="23db7-116">Eine Entität erstellt den Kontext, bevor Sie zuerst auf die TSB zugreift und den Kontext verwaltet, bis die TSB-Zugriffe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="23db7-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="23db7-117">Im Fall eines TSS würde beispielsweise die TSS-Funktion (TCG Core Services) des TSS einen TSB-Kontext erstellen, wenn er gestartet wird, und diesen Kontext so lange aktiv bleiben, bis er heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="23db7-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="23db7-118">Für Windows Server 2008 und Windows Vista schränkt TSB den Zugriff auf die TSB-API für die \\ NetworkService-Konten "Administratoren", "NT Authority LocalService" und "NT Authority" ein \\ .</span><span class="sxs-lookup"><span data-stu-id="23db7-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="23db7-119">Standardmäßig sind diese Konten die einzigen Konten, mit denen eine Verbindung mit TSB hergestellt und Kontexte erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="23db7-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="23db7-120">Zugriffsbeschränkungen können durch Erstellen eines Registrierungsschlüssel **Zugriffs** mit einem Registrierungs Wert Namen für Zeichen folgen (**reg \_ SZ**) **securityDescriptor** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="23db7-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="23db7-121">Datentyp</span><span class="sxs-lookup"><span data-stu-id="23db7-121">Data type</span></span>
</dt> <dd><span data-ttu-id="23db7-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="23db7-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="23db7-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="23db7-123">Example:</span></span>

<span data-ttu-id="23db7-124">**O:Bag: Bad: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**</span><span class="sxs-lookup"><span data-stu-id="23db7-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="23db7-125">Standardmäßig beträgt die maximale Anzahl der von TSB unterstützten Kontexte 25.</span><span class="sxs-lookup"><span data-stu-id="23db7-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="23db7-126">Diese Nummer kann geändert werden, indem Sie einen **DWORD** -Registrierungs Wert mit dem Namen " **maxkontexte** " unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **TPM** erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="23db7-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="23db7-127">Die echt Zeitverwendung des TSB-Kontexts kann mithilfe des Leistungs Monitor Tools zum Nachverfolgen der Anzahl von TSB-Kontexten beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="23db7-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="23db7-128">Für Windows 8, Windows Server 2012 und höher, ermöglicht die TSB den Zugriff auf Standardbenutzer und-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="23db7-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="23db7-129">Die Registrierungsschlüssel **securityDescriptor** und **maxkontexte** wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="23db7-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="23db7-130">Für Windows 8, Windows Server 2012 und höher, schränkt TSB den Zugriff auf bestimmte Befehle mithilfe der Befehls Blockierung ein.</span><span class="sxs-lookup"><span data-stu-id="23db7-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="23db7-131">Für Windows 10, Version 1607, ermöglicht die TSB den Zugriff von appcontainer-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="23db7-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="23db7-132">Für jede TPM-Version wurden die Schlüssel **blockedappcontainercommands** und **AllowedW8AppContainerCommands** mit den entsprechenden Listen der gesperrten bzw. zulässigen TPM-Befehle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="23db7-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="23db7-133">Für Windows 10, Version 1803, werden die Registrierungsschlüssel unter **AllowedW8AppContainerCommands** nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23db7-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




