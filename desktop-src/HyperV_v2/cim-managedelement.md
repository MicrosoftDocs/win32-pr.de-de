---
description: Die CIM \_ managedelta-Klasse ist eine abstrakte Klasse, die eine gemeinsame übergeordnete Klasse (oder oben in der Vererbungs Struktur) für die nicht Zuordnungs Klassen im CIM-Schema bereitstellt.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346060"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="df08c-103">CIM \_ managedelta-Klasse</span><span class="sxs-lookup"><span data-stu-id="df08c-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="df08c-104">Die **CIM \_ managedelta** -Klasse ist eine abstrakte Klasse, die eine gemeinsame übergeordnete Klasse (oder oben in der Vererbungs Struktur) für die nicht Zuordnungs Klassen im CIM-Schema bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="df08c-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="df08c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df08c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="df08c-106">Member</span><span class="sxs-lookup"><span data-stu-id="df08c-106">Members</span></span>

<span data-ttu-id="df08c-107">Die **CIM \_ managedelta** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="df08c-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="df08c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df08c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df08c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df08c-109">Properties</span></span>

<span data-ttu-id="df08c-110">Die **CIM \_ managedelta** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="df08c-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df08c-111">**Caption**</span><span class="sxs-lookup"><span data-stu-id="df08c-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df08c-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df08c-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df08c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df08c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df08c-114">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="df08c-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="df08c-115">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="df08c-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="df08c-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df08c-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df08c-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df08c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df08c-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df08c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df08c-119">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="df08c-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="df08c-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="df08c-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df08c-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df08c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df08c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df08c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df08c-123">Ein benutzerfreundlicher Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="df08c-123">A user-friendly name for the object.</span></span> <span data-ttu-id="df08c-124">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen benutzerfreundlichen Namen definieren.</span><span class="sxs-lookup"><span data-stu-id="df08c-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="df08c-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df08c-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df08c-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="df08c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df08c-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="df08c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df08c-128">Eindeutig und verdeckt identifiziert eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="df08c-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="df08c-129">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="df08c-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="df08c-130">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="df08c-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="df08c-131">Dieses Muster ähnelt der Struktur von Schema Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="df08c-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="df08c-132">Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="df08c-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="df08c-133">Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.</span><span class="sxs-lookup"><span data-stu-id="df08c-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="df08c-134">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="df08c-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="df08c-135">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="df08c-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="df08c-136">Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df08c-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df08c-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df08c-137">Requirements</span></span>



| <span data-ttu-id="df08c-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df08c-138">Requirement</span></span> | <span data-ttu-id="df08c-139">Wert</span><span class="sxs-lookup"><span data-stu-id="df08c-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df08c-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df08c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="df08c-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="df08c-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="df08c-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df08c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="df08c-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df08c-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="df08c-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="df08c-144">Namespace</span></span><br/>                | <span data-ttu-id="df08c-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="df08c-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df08c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="df08c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df08c-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="df08c-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df08c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="df08c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df08c-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df08c-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

