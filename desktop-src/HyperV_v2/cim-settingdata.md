---
description: Stellt Konfigurations-und Betriebsparameter für CIM- \_ managedelta-Instanzen dar.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216580"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="cd69f-103">CIM \_ SettingData-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd69f-103">CIM\_SettingData class</span></span>

<span data-ttu-id="cd69f-104">Stellt Konfigurations-und Betriebsparameter für [**CIM- \_ managedelta**](cim-managedelement.md) -Instanzen dar.</span><span class="sxs-lookup"><span data-stu-id="cd69f-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd69f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd69f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="cd69f-106">Member</span><span class="sxs-lookup"><span data-stu-id="cd69f-106">Members</span></span>

<span data-ttu-id="cd69f-107">Die **CIM \_ SettingData** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd69f-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cd69f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd69f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd69f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd69f-109">Properties</span></span>

<span data-ttu-id="cd69f-110">Die **CIM \_ SettingData** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd69f-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd69f-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd69f-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd69f-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd69f-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd69f-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd69f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd69f-114">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="cd69f-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="cd69f-115">Der benutzerfreundliche Name für eine Instanz dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="cd69f-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="cd69f-116">Außerdem kann der benutzerfreundliche Name als Index für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd69f-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="cd69f-117">Der Name muss innerhalb eines Namespace nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="cd69f-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="cd69f-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd69f-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd69f-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd69f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd69f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd69f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd69f-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="cd69f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="cd69f-122">Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="cd69f-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="cd69f-123">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="cd69f-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="cd69f-124">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId-** Eigenschaft definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cd69f-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="cd69f-125">*OrgId* darf keinen Doppelpunkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd69f-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="cd69f-126">Der erste Doppelpunkt in **InstanceId** muss zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="cd69f-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="cd69f-127">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cd69f-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="cd69f-128">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd69f-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="cd69f-129">Für von DMTF definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf "CIM" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cd69f-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd69f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd69f-130">Requirements</span></span>



| <span data-ttu-id="cd69f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd69f-131">Requirement</span></span> | <span data-ttu-id="cd69f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="cd69f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd69f-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd69f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cd69f-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd69f-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cd69f-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd69f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cd69f-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd69f-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cd69f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd69f-137">Namespace</span></span><br/>                | <span data-ttu-id="cd69f-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd69f-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd69f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cd69f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd69f-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd69f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd69f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cd69f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd69f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd69f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd69f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd69f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd69f-144">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="cd69f-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

