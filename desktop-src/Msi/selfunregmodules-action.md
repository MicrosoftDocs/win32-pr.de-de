---
description: Mit der Aktion selfunregmodules werden alle in der Tabelle selfreg aufgeführten Module, deren deinstallieren geplant ist, aufgehoben. Das Installationsprogramm führt keine Selbstregistrierung durch. EXE-Dateien.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Selfunregmodules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357073"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="74966-104">Selfunregmodules-Aktion</span><span class="sxs-lookup"><span data-stu-id="74966-104">SelfUnregModules Action</span></span>

<span data-ttu-id="74966-105">Mit der Aktion selfunregmodules werden alle in der [Tabelle selfreg](selfreg-table.md) aufgeführten Module, deren deinstallieren geplant ist, aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="74966-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="74966-106">Das Installationsprogramm führt keine Selbstregistrierung durch. EXE-Dateien.</span><span class="sxs-lookup"><span data-stu-id="74966-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="74966-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="74966-107">Sequence Restrictions</span></span>

<span data-ttu-id="74966-108">Die [InstallValidate](installvalidate-action.md) -Aktion muss vor der selfunregmodules-Aktion in der Sequenz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74966-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="74966-109">Wenn eine [SelfRegModules](selfregmodules-action.md) -Aktion verwendet wird, muss Sie nach der selfunregmodules-Aktion in der Sequenz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74966-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="74966-110">Wenn eine [RemoveFiles-Aktion](removefiles-action.md) verwendet wird, muss Sie nach der selfunregmodules-Aktion in der Sequenz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74966-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="74966-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="74966-111">ActionData Messages</span></span>



| <span data-ttu-id="74966-112">Feld</span><span class="sxs-lookup"><span data-stu-id="74966-112">Field</span></span> | <span data-ttu-id="74966-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="74966-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="74966-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="74966-114">\[1\]</span></span> | <span data-ttu-id="74966-115">Bezeichner der nicht registrierten Modul Datei.</span><span class="sxs-lookup"><span data-stu-id="74966-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="74966-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="74966-116">\[2\]</span></span> | <span data-ttu-id="74966-117">Bezeichner des Ordners, der die nicht registrierte Modul Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="74966-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="74966-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74966-118">Remarks</span></span>

<span data-ttu-id="74966-119">Die selfunregmodules-Aktion versucht, die [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) -Funktion des Moduls aufzurufen, dessen Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="74966-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="74966-120">Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erweiterten Berechtigungen ausgeführt wird, z. b. während einer Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="74966-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="74966-121">Während einer Installation pro Benutzer führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="74966-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="74966-122">Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der das Installationsprogramm die Registrierung selbst Registrierender DLLs mithilfe der selfunregmodules-Aktion aufgehoben hat.</span><span class="sxs-lookup"><span data-stu-id="74966-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74966-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74966-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74966-124">Angeben der Reihenfolge der Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="74966-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
