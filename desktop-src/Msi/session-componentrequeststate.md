---
description: Die componentrequeststate-Eigenschaft des Session-Objekts Ruft eine Änderung im Aktionszustand einer Zeile in der Komponenten Tabelle ab oder fordert Sie an.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session. componentrequeststate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368473"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="807ad-103">Session. componentrequeststate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="807ad-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="807ad-104">Die **componentrequeststate** -Eigenschaft des [**Session**](session-object.md) -Objekts Ruft eine Änderung im Aktionszustand einer Zeile in der [Komponenten Tabelle](component-table.md)ab oder fordert Sie an.</span><span class="sxs-lookup"><span data-stu-id="807ad-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="807ad-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="807ad-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="807ad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="807ad-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="807ad-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="807ad-107">Property value</span></span>

<span data-ttu-id="807ad-108">Erforderlicher Zeichen folgen Name des Komponenten Elements, Primärschlüssel der Komponenten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="807ad-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="807ad-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="807ad-109">Remarks</span></span>



| <span data-ttu-id="807ad-110">Auswahl Status</span><span class="sxs-lookup"><span data-stu-id="807ad-110">Selection state</span></span>        | <span data-ttu-id="807ad-111">Wert</span><span class="sxs-lookup"><span data-stu-id="807ad-111">Value</span></span> | <span data-ttu-id="807ad-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="807ad-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="807ad-113">Null</span><span class="sxs-lookup"><span data-stu-id="807ad-113">Null</span></span>                   | <span data-ttu-id="807ad-114">Null</span><span class="sxs-lookup"><span data-stu-id="807ad-114">Null</span></span>  | <span data-ttu-id="807ad-115">Fordert an, dass für dieses Element keine Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="807ad-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="807ad-116">msiinstallstatemissing</span><span class="sxs-lookup"><span data-stu-id="807ad-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="807ad-117">2</span><span class="sxs-lookup"><span data-stu-id="807ad-117">2</span></span>     | <span data-ttu-id="807ad-118">Das Element muss entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="807ad-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="807ad-119">msiinstallstatuelocal</span><span class="sxs-lookup"><span data-stu-id="807ad-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="807ad-120">3</span><span class="sxs-lookup"><span data-stu-id="807ad-120">3</span></span>     | <span data-ttu-id="807ad-121">Das Element muss lokal installiert werden.</span><span class="sxs-lookup"><span data-stu-id="807ad-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="807ad-122">msiinstallstaatource</span><span class="sxs-lookup"><span data-stu-id="807ad-122">msiInstallStateSource</span></span>  | <span data-ttu-id="807ad-123">4</span><span class="sxs-lookup"><span data-stu-id="807ad-123">4</span></span>     | <span data-ttu-id="807ad-124">Das Element muss installiert und vom Quell Medium aus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="807ad-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="807ad-125">msiinstallstatedefault</span><span class="sxs-lookup"><span data-stu-id="807ad-125">msiInstallStateDefault</span></span> | <span data-ttu-id="807ad-126">5</span><span class="sxs-lookup"><span data-stu-id="807ad-126">5</span></span>     | <span data-ttu-id="807ad-127">Wenn das Element installiert ist, muss es im selben Zustand neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="807ad-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="807ad-128">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="807ad-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="807ad-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="807ad-129">Requirements</span></span>



| <span data-ttu-id="807ad-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="807ad-130">Requirement</span></span> | <span data-ttu-id="807ad-131">Wert</span><span class="sxs-lookup"><span data-stu-id="807ad-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="807ad-132">Version</span><span class="sxs-lookup"><span data-stu-id="807ad-132">Version</span></span><br/> | <span data-ttu-id="807ad-133">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="807ad-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="807ad-134">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="807ad-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="807ad-135">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="807ad-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="807ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="807ad-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="807ad-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="807ad-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="807ad-138">IID</span><span class="sxs-lookup"><span data-stu-id="807ad-138">IID</span></span><br/>     | <span data-ttu-id="807ad-139">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="807ad-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




