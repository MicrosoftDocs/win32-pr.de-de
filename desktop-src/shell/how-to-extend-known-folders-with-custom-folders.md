---
description: Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem Sie bekannte Ordner eigenständig registrieren.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Erweitern bekannter Ordner mit benutzerdefinierten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215942"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="460b4-103">Erweitern bekannter Ordner mit benutzerdefinierten Ordnern</span><span class="sxs-lookup"><span data-stu-id="460b4-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="460b4-104">Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner auf einem System erweitern, indem Sie bekannte Ordner eigenständig registrieren.</span><span class="sxs-lookup"><span data-stu-id="460b4-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="460b4-105">Nach der Registrierung sind die Ordner von Drittanbietern dem System bekannt.</span><span class="sxs-lookup"><span data-stu-id="460b4-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="460b4-106">Sie werden durch einen beliebigen Aufrufen von [**iknownfoldermanager:: getfolderids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)gefunden.</span><span class="sxs-lookup"><span data-stu-id="460b4-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="460b4-107">Beachten Sie, dass ein bekannter Ordner ein Ordner pro Computer sein muss.</span><span class="sxs-lookup"><span data-stu-id="460b4-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="460b4-108">Es ist nicht möglich, einen pro Benutzer bekannten Ordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="460b4-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="460b4-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="460b4-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="460b4-110">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="460b4-110">Step 1:</span></span>

<span data-ttu-id="460b4-111">Definieren Sie ihren bekannten Ordner über eine [**knownfolder- \_ Definitions**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) Struktur.</span><span class="sxs-lookup"><span data-stu-id="460b4-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="460b4-112">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="460b4-112">Step 2:</span></span>

<span data-ttu-id="460b4-113">Registrieren Sie den bekannten Ordner durch einen [**iknownfoldermanager:: registerfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="460b4-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="460b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="460b4-114">Remarks</span></span>

<span data-ttu-id="460b4-115">Wenn Sie einen bekannten Ordner für Ihre Anwendung als Teil des Installationsvorgangs erstellen, müssen Sie auch [**iknownfoldermanager:: unregisterfolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) als Teil Ihres uninstallationscodes einschließen.</span><span class="sxs-lookup"><span data-stu-id="460b4-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="460b4-116">Berücksichtigen Sie, warum der Ordner vor der Registrierung in das bekannte Ordnersystem aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="460b4-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="460b4-117">Sie sollten einen gültigen Grund haben, den Ordner auf diese Ebene der System Sichtbarkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="460b4-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="460b4-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="460b4-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="460b4-119">[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="460b4-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
