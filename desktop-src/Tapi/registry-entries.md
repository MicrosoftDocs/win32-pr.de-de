---
description: Die austauschbaren Terminals werden in Terminal SuperClasses klassifiziert.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Registrierungseinträge (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357125"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="a6840-103">Registrierungseinträge (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="a6840-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="a6840-104">Die austauschbaren Terminals werden in Terminal SuperClasses klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="a6840-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="a6840-105">Jede Terminal Superclass verfügt über einen Eintrag in der Registrierung unter folgendem Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="a6840-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="a6840-106">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telefonie** \\ **Terminalmanager**</span><span class="sxs-lookup"><span data-stu-id="a6840-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="a6840-107">Unter dem Schlüssel "Terminal Superclass" finden Sie Einträge für jedes austauschbare Terminal innerhalb der Terminal-Superclass.</span><span class="sxs-lookup"><span data-stu-id="a6840-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="a6840-108">Der Eintrag für jede Terminal Superclass wird durch eine Terminal-Superclass-CLSID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a6840-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="a6840-109">Dies ist ein eindeutiger Bezeichner für eine Terminal Klasse.</span><span class="sxs-lookup"><span data-stu-id="a6840-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="a6840-110">Die Terminal Klasse verfügt über ein optionales Attribut: Name, bei dem es sich um einen anzeigen Amen für die Terminal Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="a6840-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="a6840-111">Jedes austauschbare Terminal wird durch eine CLSID-Terminal Klasse identifiziert. Das heißt, eine GUID.</span><span class="sxs-lookup"><span data-stu-id="a6840-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="a6840-112">Die Attribute für austauschbares Terminal werden in austauschbaren Terminal Schlüsselwerten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a6840-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="a6840-113">Die Attribute für ein austauschbares Terminal sind die folgenden.</span><span class="sxs-lookup"><span data-stu-id="a6840-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="a6840-114">Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="a6840-114">Terminal class</span></span> | <span data-ttu-id="a6840-115">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="a6840-115">Key name</span></span> | <span data-ttu-id="a6840-116">Öffentlicher Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a6840-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a6840-117">Name</span><span class="sxs-lookup"><span data-stu-id="a6840-117">Name</span></span>           | <span data-ttu-id="a6840-118">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a6840-118">REG\_SZ</span></span>  | <span data-ttu-id="a6840-119">Anzeige Name für das Terminal</span><span class="sxs-lookup"><span data-stu-id="a6840-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="a6840-120">Company</span><span class="sxs-lookup"><span data-stu-id="a6840-120">Company</span></span>        | <span data-ttu-id="a6840-121">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a6840-121">REG\_SZ</span></span>  | <span data-ttu-id="a6840-122">Unternehmensname</span><span class="sxs-lookup"><span data-stu-id="a6840-122">Company name</span></span>                                                                      |
| <span data-ttu-id="a6840-123">Version</span><span class="sxs-lookup"><span data-stu-id="a6840-123">Version</span></span>        | <span data-ttu-id="a6840-124">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a6840-124">REG\_SZ</span></span>  | <span data-ttu-id="a6840-125">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="a6840-125">Version information</span></span>                                                               |
| <span data-ttu-id="a6840-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="a6840-126">CLSID</span></span>          | <span data-ttu-id="a6840-127">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a6840-127">REG\_SZ</span></span>  | <span data-ttu-id="a6840-128">Terminal-CLSID (in com [**cokreatumstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode verwendet)</span><span class="sxs-lookup"><span data-stu-id="a6840-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="a6840-129">Wegbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="a6840-129">Directions</span></span>     | <span data-ttu-id="a6840-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="a6840-130">DWORD</span></span>    | <span data-ttu-id="a6840-131">Terminal Richtung</span><span class="sxs-lookup"><span data-stu-id="a6840-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="a6840-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="a6840-132">MediaTypes</span></span>     | <span data-ttu-id="a6840-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="a6840-133">DWORD</span></span>    | <span data-ttu-id="a6840-134">Unterstützte Terminal Medientypen</span><span class="sxs-lookup"><span data-stu-id="a6840-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="a6840-135">Bei einer Terminal Klasse sind die Attribute wie folgt.</span><span class="sxs-lookup"><span data-stu-id="a6840-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="a6840-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="a6840-136">CLSID</span></span> | <span data-ttu-id="a6840-137">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="a6840-137">Key name</span></span> | <span data-ttu-id="a6840-138">Öffentlicher Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a6840-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="a6840-139">Name</span><span class="sxs-lookup"><span data-stu-id="a6840-139">Name</span></span>  | <span data-ttu-id="a6840-140">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a6840-140">REG\_SZ</span></span>  | <span data-ttu-id="a6840-141">Anzeige Name der Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="a6840-141">Terminal class friendly name</span></span> |



 

 

 
