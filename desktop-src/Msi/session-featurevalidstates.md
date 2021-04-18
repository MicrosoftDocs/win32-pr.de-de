---
description: Die featurevalidstates-Eigenschaft des Session-Objekts gibt eine ganze Zahl zurück, die Bitflags mit jedem relevanten Bit darstellt, das einen gültigen Installations Zustand für das angegebene Feature darstellt.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session. featurevalidstates (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365706"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="88c83-103">Session. featurevalidstates (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88c83-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="88c83-104">Die **featurevalidstates** -Eigenschaft des [**Session**](session-object.md) -Objekts gibt eine ganze Zahl zurück, die Bitflags mit jedem relevanten Bit darstellt, das einen gültigen Installations Zustand für das angegebene Feature darstellt.</span><span class="sxs-lookup"><span data-stu-id="88c83-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="88c83-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="88c83-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c83-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="88c83-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="88c83-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="88c83-107">Property value</span></span>

<span data-ttu-id="88c83-108">Erforderlicher Zeichen folgen Name des Funktions Elements, dessen gültige Installations Zustände abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="88c83-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="88c83-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88c83-109">Remarks</span></span>

<span data-ttu-id="88c83-110">Der Rückgabewert besteht wie folgt aus Bitflags.</span><span class="sxs-lookup"><span data-stu-id="88c83-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="88c83-111">Bit 0: Wenn festgelegt, ist Local ein gültiger Zustand.</span><span class="sxs-lookup"><span data-stu-id="88c83-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="88c83-112">Bit 1: Wenn festgelegt, ist die Quelle ein gültiger Zustand.</span><span class="sxs-lookup"><span data-stu-id="88c83-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="88c83-113">Die **featurevalidstates** -Eigenschaft ist nur erfolgreich, nachdem das Installationsprogramm die Aktionen " [costinitialize](costinitialize-action.md) " und " [costfinalize](costfinalize-action.md) " aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="88c83-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="88c83-114">**Featurevalidstates** bestimmt die Zustands Gültigkeit, indem alle Komponenten abgefragt werden, die mit der angegebenen Funktion verknüpft sind, ohne den aktuell installierten Zustand einer beliebigen Komponente zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="88c83-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="88c83-115">Die möglichen gültigen Zustände für eine Funktion werden wie folgt bestimmt:</span><span class="sxs-lookup"><span data-stu-id="88c83-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="88c83-116">Wenn die Funktion keine Komponenten enthält, sind sowohl InstallState \_ local als auch InstallState \_ Source gültige Zustände für das Feature.</span><span class="sxs-lookup"><span data-stu-id="88c83-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="88c83-117">Wenn mindestens eine Komponente der Funktion über das Attribut "msidbcomponentattributeslocalonly" oder "msidbcomponentattributesoptional" verfügt, ist "InstallState \_ local" ein gültiger Status für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="88c83-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="88c83-118">Wenn mindestens eine Komponente der Funktion über ein Attribut von msidbcomponentattributessourceonly oder msidbcomponentattributesoptionalen verfügt, ist die InstallState- \_ Quelle ein gültiger Status für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="88c83-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="88c83-119">Wenn eine Datei einer Komponente, die zur Funktion gehört, gepatcht wird oder aus einer komprimierten Quelle entfernt wird, ist die InstallState- \_ Quelle nicht als gültiger Status für das Feature enthalten.</span><span class="sxs-lookup"><span data-stu-id="88c83-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="88c83-120">Die InstallState-Ankündigung \_ ist kein gültiger Status, wenn die Funktion keine Ankündigung zulässt (msidbfeatureattributesdisallowankündigungs), oder die Funktion erfordert Platt Form Unterstützung für Ankündigungen (msidbfeatureattributesnounsupportedankündigungs Ankündigung), und die Plattform unterstützt diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="88c83-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="88c83-121">"InstallState \_ Missing" ist ein gültiger Status für die Funktion, wenn die Attribute "msidbfeatureattributesuidisallowmissing" nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="88c83-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="88c83-122">Gültige Zustände für untergeordnete Funktionen, die für die übergeordnete Funktion gekennzeichnet sind (msidbfeatureattributesfollowparent), basieren auf der Aktion oder dem installierten Status der übergeordneten Funktion.</span><span class="sxs-lookup"><span data-stu-id="88c83-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="88c83-123">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="88c83-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88c83-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88c83-124">Requirements</span></span>



| <span data-ttu-id="88c83-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88c83-125">Requirement</span></span> | <span data-ttu-id="88c83-126">Wert</span><span class="sxs-lookup"><span data-stu-id="88c83-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c83-127">Version</span><span class="sxs-lookup"><span data-stu-id="88c83-127">Version</span></span><br/> | <span data-ttu-id="88c83-128">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88c83-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88c83-129">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88c83-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88c83-130">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="88c83-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="88c83-131">DLL</span><span class="sxs-lookup"><span data-stu-id="88c83-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="88c83-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88c83-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="88c83-133">IID</span><span class="sxs-lookup"><span data-stu-id="88c83-133">IID</span></span><br/>     | <span data-ttu-id="88c83-134">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="88c83-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




