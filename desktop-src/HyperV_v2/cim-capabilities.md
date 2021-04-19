---
description: Eine abstrakte Klasse für Unterklassen, die die Fähigkeiten eines zugeordneten verwalteten Elements beschreibt, und das Potenzial der Fähigkeiten.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349925"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="0fd3c-103">CIM-Funktions \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="0fd3c-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="0fd3c-104">Eine abstrakte Klasse für Unterklassen, die die Fähigkeiten eines zugeordneten verwalteten Elements beschreibt, und das Potenzial der Fähigkeiten.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd3c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="0fd3c-106">Member</span><span class="sxs-lookup"><span data-stu-id="0fd3c-106">Members</span></span>

<span data-ttu-id="0fd3c-107">Die **CIM \_** -Funktionsklasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0fd3c-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0fd3c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fd3c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fd3c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fd3c-109">Properties</span></span>

<span data-ttu-id="0fd3c-110">Die **CIM \_** -Funktionsklasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fd3c-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0fd3c-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd3c-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fd3c-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fd3c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fd3c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd3c-114">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="0fd3c-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="0fd3c-115">Der benutzerfreundliche Name für diese Klasseninstanz.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="0fd3c-116">Außerdem kann der benutzerfreundliche Name als Index Eigenschaft für eine Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="0fd3c-117">Dieser Wert muss innerhalb des Namespace nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="0fd3c-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0fd3c-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd3c-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0fd3c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fd3c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0fd3c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd3c-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="0fd3c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="0fd3c-122">Eindeutig und verdeckt identifiziert eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="0fd3c-123">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="0fd3c-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="0fd3c-124">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="0fd3c-125">Dieses Muster ähnelt der Struktur von Schema Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="0fd3c-126">Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="0fd3c-127">Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="0fd3c-128">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="0fd3c-129">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="0fd3c-130">Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fd3c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fd3c-131">Requirements</span></span>



| <span data-ttu-id="0fd3c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fd3c-132">Requirement</span></span> | <span data-ttu-id="0fd3c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0fd3c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd3c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fd3c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd3c-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0fd3c-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0fd3c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fd3c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd3c-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fd3c-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0fd3c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fd3c-138">Namespace</span></span><br/>                | <span data-ttu-id="0fd3c-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0fd3c-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0fd3c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0fd3c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fd3c-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fd3c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd3c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd3c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0fd3c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd3c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd3c-145">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="0fd3c-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

