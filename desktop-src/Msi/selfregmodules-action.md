---
description: Die SelfRegModules-Aktion verarbeitet alle in der Tabelle selfreg aufgeführten Module und registriert alle installierten Module beim System. Der Installer führt keine Selbstregistrierung von exe-Dateien durch.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: SelfRegModules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352584"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="5a9ca-104">SelfRegModules-Aktion</span><span class="sxs-lookup"><span data-stu-id="5a9ca-104">SelfRegModules Action</span></span>

<span data-ttu-id="5a9ca-105">Die SelfRegModules-Aktion verarbeitet alle in der Tabelle [selfreg](selfreg-table.md) aufgeführten Module und registriert alle installierten Module beim System.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="5a9ca-106">Der Installer führt keine Selbstregistrierung von exe-Dateien durch.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5a9ca-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5a9ca-107">Sequence Restrictions</span></span>

<span data-ttu-id="5a9ca-108">Die [InstallValidate](installvalidate-action.md) -Aktion muss aufgerufen werden, bevor die SelfRegModules-Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="5a9ca-109">Wenn eine [InstallFiles](installfiles-action.md) -Aktion verwendet wird, muss Sie vor der SelfRegModules-Aktion in der Sequenz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="5a9ca-110">Da die SelfRegModules-Aktion das System ändert, sollte SelfRegModules nach der [InstallInitialize-Aktion](installinitialize-action.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5a9ca-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="5a9ca-111">ActionData Messages</span></span>



| <span data-ttu-id="5a9ca-112">Feld</span><span class="sxs-lookup"><span data-stu-id="5a9ca-112">Field</span></span> | <span data-ttu-id="5a9ca-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="5a9ca-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="5a9ca-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5a9ca-114">\[1\]</span></span> | <span data-ttu-id="5a9ca-115">Bezeichner der registrierten Modul Datei.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="5a9ca-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5a9ca-116">\[2\]</span></span> | <span data-ttu-id="5a9ca-117">Bezeichner des Ordners mit der registrierten Modul Datei.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5a9ca-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a9ca-118">Remarks</span></span>

<span data-ttu-id="5a9ca-119">Die SelfRegModules-Aktion versucht, die [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Funktion des Moduls, das für die Registrierung geplant ist, aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="5a9ca-120">Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erweiterten Berechtigungen ausgeführt wird, z. b. während einer Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="5a9ca-121">Bei einer pro-Benutzer-Installation führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="5a9ca-122">Beachten Sie, dass Sie die Reihenfolge, in der der Installer selbst Registrierungs-DLLs registriert, nicht mithilfe der [selfunregmodules-Aktion](selfunregmodules-action.md)angeben können.</span><span class="sxs-lookup"><span data-stu-id="5a9ca-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a9ca-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a9ca-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9ca-124">Angeben der Reihenfolge der Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="5a9ca-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
