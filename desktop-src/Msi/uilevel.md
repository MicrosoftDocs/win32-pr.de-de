---
description: Der Installer legt die uilevel-Eigenschaft auf die Ebene der Benutzeroberfläche fest.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Uilevel-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368524"
---
# <a name="uilevel-property"></a><span data-ttu-id="ad284-103">Uilevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad284-103">UILevel property</span></span>

<span data-ttu-id="ad284-104">Der Installer legt die **uilevel** -Eigenschaft auf die Ebene der Benutzeroberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="ad284-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="ad284-105">Die interne Benutzeroberfläche wird von [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)aktiviert und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad284-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="ad284-106">Diese Eigenschaft wird auf einen der folgenden installuilevel-Datentypen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad284-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="ad284-107">Installuilevel</span><span class="sxs-lookup"><span data-stu-id="ad284-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="ad284-108">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="ad284-108">Numeric value</span></span> | <span data-ttu-id="ad284-109">Benutzeroberflächen Ebene</span><span class="sxs-lookup"><span data-stu-id="ad284-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="ad284-110">installuilevel \_ None</span><span class="sxs-lookup"><span data-stu-id="ad284-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="ad284-111">2</span><span class="sxs-lookup"><span data-stu-id="ad284-111">2</span></span>             | <span data-ttu-id="ad284-112">Vollständig automatische Installation:</span><span class="sxs-lookup"><span data-stu-id="ad284-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="ad284-113">installuilevel \_ Basic</span><span class="sxs-lookup"><span data-stu-id="ad284-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="ad284-114">3</span><span class="sxs-lookup"><span data-stu-id="ad284-114">3</span></span>             | <span data-ttu-id="ad284-115">Einfacher Fortschritt und Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="ad284-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="ad284-116">installuilevel \_ reduziert</span><span class="sxs-lookup"><span data-stu-id="ad284-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="ad284-117">4</span><span class="sxs-lookup"><span data-stu-id="ad284-117">4</span></span>             | <span data-ttu-id="ad284-118">Erstellte Benutzeroberfläche, Assistenten Dialogfelder werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="ad284-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="ad284-119">installuilevel \_ voll</span><span class="sxs-lookup"><span data-stu-id="ad284-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="ad284-120">5</span><span class="sxs-lookup"><span data-stu-id="ad284-120">5</span></span>             | <span data-ttu-id="ad284-121">Erstellte Benutzeroberfläche mit Assistenten, Fortschritt, Fehlern.</span><span class="sxs-lookup"><span data-stu-id="ad284-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ad284-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad284-122">Requirements</span></span>



| <span data-ttu-id="ad284-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad284-123">Requirement</span></span> | <span data-ttu-id="ad284-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ad284-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad284-125">Version</span><span class="sxs-lookup"><span data-stu-id="ad284-125">Version</span></span><br/> | <span data-ttu-id="ad284-126">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad284-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ad284-127">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ad284-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ad284-128">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ad284-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ad284-129">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ad284-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad284-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad284-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad284-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad284-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ad284-132">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ad284-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="ad284-133">Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="ad284-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




