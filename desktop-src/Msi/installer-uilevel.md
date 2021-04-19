---
description: Die uilevel-Eigenschaft des Installer-Objekts ist eine Lese-/Schreibeigenschaft, die den Typ der zu verwendenden Benutzeroberfläche angibt, wenn nachfolgende Pakete im aktuellen Prozessbereich geöffnet und verarbeitet werden.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer. uilevel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362142"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="c5873-103">Installer. uilevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5873-103">Installer.UILevel property</span></span>

<span data-ttu-id="c5873-104">Die **uilevel** -Eigenschaft des [**Installer**](installer-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Typ der zu verwendenden Benutzeroberfläche angibt, wenn nachfolgende Pakete im aktuellen Prozessbereich geöffnet und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c5873-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="c5873-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c5873-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5873-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5873-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="c5873-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c5873-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c5873-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5873-108">Remarks</span></span>



| <span data-ttu-id="c5873-109">Benutzeroberflächen Ebene</span><span class="sxs-lookup"><span data-stu-id="c5873-109">User interface level</span></span>   | <span data-ttu-id="c5873-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c5873-110">Value</span></span> | <span data-ttu-id="c5873-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5873-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5873-112">msiuilevelnochange</span><span class="sxs-lookup"><span data-stu-id="c5873-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="c5873-113">0</span><span class="sxs-lookup"><span data-stu-id="c5873-113">0</span></span>     | <span data-ttu-id="c5873-114">Ändert die Benutzeroberflächen Ebene nicht.</span><span class="sxs-lookup"><span data-stu-id="c5873-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c5873-115">msiuileveldefault</span><span class="sxs-lookup"><span data-stu-id="c5873-115">msiUILevelDefault</span></span>      | <span data-ttu-id="c5873-116">1</span><span class="sxs-lookup"><span data-stu-id="c5873-116">1</span></span>     | <span data-ttu-id="c5873-117">Verwendet die standardmäßige Benutzeroberflächen Ebene.</span><span class="sxs-lookup"><span data-stu-id="c5873-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="c5873-118">msiuilevelnone</span><span class="sxs-lookup"><span data-stu-id="c5873-118">msiUILevelNone</span></span>         | <span data-ttu-id="c5873-119">2</span><span class="sxs-lookup"><span data-stu-id="c5873-119">2</span></span>     | <span data-ttu-id="c5873-120">Automatische Installation.</span><span class="sxs-lookup"><span data-stu-id="c5873-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c5873-121">msiuilevelbasic</span><span class="sxs-lookup"><span data-stu-id="c5873-121">msiUILevelBasic</span></span>        | <span data-ttu-id="c5873-122">3</span><span class="sxs-lookup"><span data-stu-id="c5873-122">3</span></span>     | <span data-ttu-id="c5873-123">Einfacher Fortschritt und Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="c5873-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c5873-124">msiuilevelreduced</span><span class="sxs-lookup"><span data-stu-id="c5873-124">msiUILevelReduced</span></span>      | <span data-ttu-id="c5873-125">4</span><span class="sxs-lookup"><span data-stu-id="c5873-125">4</span></span>     | <span data-ttu-id="c5873-126">Die Benutzeroberfläche und die Dialogfelder der Assistenten wurden unterdrückt</span><span class="sxs-lookup"><span data-stu-id="c5873-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c5873-127">msiuilevelfull</span><span class="sxs-lookup"><span data-stu-id="c5873-127">msiUILevelFull</span></span>         | <span data-ttu-id="c5873-128">5</span><span class="sxs-lookup"><span data-stu-id="c5873-128">5</span></span>     | <span data-ttu-id="c5873-129">Erstellte Benutzeroberfläche mit Assistenten, Fortschritt und Fehlern.</span><span class="sxs-lookup"><span data-stu-id="c5873-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c5873-130">msiuilevelhidecancel</span><span class="sxs-lookup"><span data-stu-id="c5873-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="c5873-131">32</span><span class="sxs-lookup"><span data-stu-id="c5873-131">32</span></span>    | <span data-ttu-id="c5873-132">In Kombination mit dem Wert von "msiuilevelbasic" zeigt das Installationsprogramm Status Dialogfelder an, zeigt jedoch keine Schaltfläche **Abbrechen** im Dialogfeld an, um zu verhindern, dass die Installation von Benutzern abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="c5873-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="c5873-133">msiuilevelprogressonly</span><span class="sxs-lookup"><span data-stu-id="c5873-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="c5873-134">64</span><span class="sxs-lookup"><span data-stu-id="c5873-134">64</span></span>    | <span data-ttu-id="c5873-135">In Kombination mit dem Wert von "msiuilevelbasic" zeigt das Installationsprogramm Status Dialogfelder an, zeigt jedoch keine modalen Dialogfelder oder Fehler Dialogfelder an.</span><span class="sxs-lookup"><span data-stu-id="c5873-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="c5873-136">msiuilevelenddialog</span><span class="sxs-lookup"><span data-stu-id="c5873-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="c5873-137">128</span><span class="sxs-lookup"><span data-stu-id="c5873-137">128</span></span>   | <span data-ttu-id="c5873-138">In Kombination mit einem der obigen Werte zeigt das Installationsprogramm am Ende einer erfolgreichen Installation ein modales Dialogfeld an, oder wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c5873-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="c5873-139">Wenn der Benutzer abbricht, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5873-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="c5873-140">Weitere Informationen finden Sie unter [bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="c5873-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5873-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5873-141">Requirements</span></span>



| <span data-ttu-id="c5873-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5873-142">Requirement</span></span> | <span data-ttu-id="c5873-143">Wert</span><span class="sxs-lookup"><span data-stu-id="c5873-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5873-144">Version</span><span class="sxs-lookup"><span data-stu-id="c5873-144">Version</span></span><br/> | <span data-ttu-id="c5873-145">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5873-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5873-146">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5873-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5873-147">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5873-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c5873-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c5873-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5873-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5873-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c5873-150">IID</span><span class="sxs-lookup"><span data-stu-id="c5873-150">IID</span></span><br/>     | <span data-ttu-id="c5873-151">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c5873-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




