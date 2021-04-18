---
description: Die featurerequeststate-Eigenschaft ist eine Lese-/Schreibeigenschaft des Session-Objekts.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session. featurerequeststate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368518"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="a0bdd-103">Session. featurerequeststate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a0bdd-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="a0bdd-104">Die **featurerequeststate** -Eigenschaft ist eine Lese-/Schreibeigenschaft des [**Session**](session-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="a0bdd-105">Sie kann verwendet werden, um den aktuellen Aktionszustand eines Features zu erhalten oder eine Änderung der Aktion einer Funktion und ihrer untergeordneten Funktionen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="a0bdd-106">Die [Funktion muss](feature-table.md) in der Featuretabelle benannt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="a0bdd-107">Wenn eine Änderung des Aktions Zustands eines Features angefordert wird, kann auch der Aktions Status aller Komponenten des geänderten Features geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="a0bdd-108">Der Aktions Status von Komponenten, die von mehreren Features gemeinsam verwendet werden, wird je nach dem Status der neuen Funktions Aktion entsprechend geändert (siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="a0bdd-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="a0bdd-109">Die **featurerequeststate** -Eigenschaft kann auch verwendet werden, um alle Features gleichzeitig zu konfigurieren, indem das Schlüsselwort all anstelle eines bestimmten Featurenamens angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="a0bdd-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bdd-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0bdd-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="a0bdd-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a0bdd-112">Property value</span></span>

<span data-ttu-id="a0bdd-113">Erforderliche Zeichenfolge, die den Namen des zu konfigurierenden Features angibt.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="a0bdd-114">Um alle Funktionen auf einen gewünschten Anforderungs Status festzulegen, verwenden Sie die reservierte Groß-/Kleinschreibung nicht.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0bdd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0bdd-115">Remarks</span></span>

<span data-ttu-id="a0bdd-116">Die [**setinstalllevel**](session-setinstalllevel.md) -Methode muss vor dem Aufruf von **featurerequeststate** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="a0bdd-117">Wenn der aktuelle Status der Funktion angefordert wird, gibt die **featurerequeststate** -Eigenschaft einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="a0bdd-118">Name des Auswahl Zustands</span><span class="sxs-lookup"><span data-stu-id="a0bdd-118">Selection state name</span></span>         | <span data-ttu-id="a0bdd-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a0bdd-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a0bdd-120">msiinstallstateunknown =-1</span><span class="sxs-lookup"><span data-stu-id="a0bdd-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="a0bdd-121">Für das Feature wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-121">No action is taken for the feature.</span></span> <span data-ttu-id="a0bdd-122">Dies entspricht NULL.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="a0bdd-123">msiinstallstateangekündigten = 1</span><span class="sxs-lookup"><span data-stu-id="a0bdd-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="a0bdd-124">Das Feature muss angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="a0bdd-125">msiinstallstatemissing = 2</span><span class="sxs-lookup"><span data-stu-id="a0bdd-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="a0bdd-126">Das Feature muss entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="a0bdd-127">msiinstallstatuelocal = 3</span><span class="sxs-lookup"><span data-stu-id="a0bdd-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="a0bdd-128">Das Feature muss als "Run-local" installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="a0bdd-129">msiinstallstaatource = 4</span><span class="sxs-lookup"><span data-stu-id="a0bdd-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="a0bdd-130">Das Feature muss als "Run-From-Source" installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="a0bdd-131">msiinstallstatedefault = 5</span><span class="sxs-lookup"><span data-stu-id="a0bdd-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="a0bdd-132">Das Feature muss mit dem aktuellen Aktionszustand der Funktion neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="a0bdd-133">Der folgende Code ruft beispielsweise den aktuellen Status von "myfeature" aus einer benutzerdefinierten VBScript-Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="a0bdd-134">Wenn der Status der Funktion konfiguriert wird, sollte die Eigenschaft **featurerequeststate** auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="a0bdd-135">Name des Auswahl Zustands</span><span class="sxs-lookup"><span data-stu-id="a0bdd-135">Selection state name</span></span>          | <span data-ttu-id="a0bdd-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a0bdd-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="a0bdd-137">msiinstallstateangekündigten = 1</span><span class="sxs-lookup"><span data-stu-id="a0bdd-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="a0bdd-138">Ankündigen Sie das Feature.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="a0bdd-139">msiinstallstatemissing = 2</span><span class="sxs-lookup"><span data-stu-id="a0bdd-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="a0bdd-140">Entfernen Sie die Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="a0bdd-141">msiinstallstatuelocal = 3</span><span class="sxs-lookup"><span data-stu-id="a0bdd-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="a0bdd-142">Installieren Sie die Funktion als "Run-local".</span><span class="sxs-lookup"><span data-stu-id="a0bdd-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="a0bdd-143">msiinstallstaatource = 4</span><span class="sxs-lookup"><span data-stu-id="a0bdd-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="a0bdd-144">Installieren Sie die Funktion als "aus Quelle ausführen".</span><span class="sxs-lookup"><span data-stu-id="a0bdd-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="a0bdd-145">Beispielsweise werden die folgenden Anforderungen aus einer benutzerdefinierten VBScript-Aktion, die "myfeature" für die lokale Installation auf dem Computer installiert ist, installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="a0bdd-146">Wenn **featurerequeststate** aufgerufen wird, versucht das Installationsprogramm, den Aktionszustand für jede Komponente, die an die angegebene Funktion gebunden ist, möglichst am besten in den angegebenen Zustand zu setzen.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="a0bdd-147">Es gibt jedoch häufige Situationen, in denen die Anforderung nicht vollständig berücksichtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="a0bdd-148">Wenn z. b. eine Funktion mit zwei Komponenten verknüpft ist, die Komponente a und Komponente b durch die [FeatureComponents](featurecomponents-table.md) -Tabelle und Komponente a das **msidbcomponentattributeslocalonly** -Attribut und Komponente b das **msidbcomponentattributessourceonly** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="a0bdd-149">Wenn **featurerequeststate** in diesem Fall mit dem angeforderten Zustand msiinstallstatelocal oder msiinstallstaatource aufgerufen wird, kann die Anforderung für beide Komponenten nicht berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="a0bdd-150">In diesem Fall können beide Komponenten eingeschaltet werden, wobei Komponente a auf msiinstallstatelocal und Komponente B auf msiinstallstaatource festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="a0bdd-151">Wenn mehr als eine Funktion mit einer einzelnen Komponente verknüpft ist, wird der endgültige Aktions Status der Komponente wie folgt bestimmt: Wenn mindestens ein Feature aufruft, dass die Komponente lokal installiert werden soll, wird msiinstallstatelocal installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="a0bdd-152">Wenn mindestens ein Feature aufruft, damit die Komponente vom Quell Medium aus ausgeführt wird, wird msiinstallstaatource installiert.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="a0bdd-153">Wenn mindestens ein Feature zum Entfernen der Komponente aufruft, lautet der Aktionszustand msiinstallstatemissing.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="a0bdd-154">Weitere Informationen zur Auswahl von Features für die Installation finden Sie [in der](feature-table.md) Featuretabelle.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="a0bdd-155">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bdd-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0bdd-156">Requirements</span></span>



| <span data-ttu-id="a0bdd-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0bdd-157">Requirement</span></span> | <span data-ttu-id="a0bdd-158">Wert</span><span class="sxs-lookup"><span data-stu-id="a0bdd-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bdd-159">Version</span><span class="sxs-lookup"><span data-stu-id="a0bdd-159">Version</span></span><br/> | <span data-ttu-id="a0bdd-160">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a0bdd-161">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a0bdd-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a0bdd-162">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0bdd-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a0bdd-163">DLL</span><span class="sxs-lookup"><span data-stu-id="a0bdd-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0bdd-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0bdd-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a0bdd-165">IID</span><span class="sxs-lookup"><span data-stu-id="a0bdd-165">IID</span></span><br/>     | <span data-ttu-id="a0bdd-166">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a0bdd-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="a0bdd-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0bdd-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bdd-168">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="a0bdd-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="a0bdd-169">Feature</span><span class="sxs-lookup"><span data-stu-id="a0bdd-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




