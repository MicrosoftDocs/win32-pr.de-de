---
description: 'Weitere Informationen finden Sie unter: MofDeserializerSchemaValidationOption-Enumeration'
title: MofDeserializerSchemaValidationOption-Enumeration (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: MofDeserializerSchemaValidationOption enumeration (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
ms.date: 11/14/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Default
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Strict
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Loose
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::IgnorePropertyType
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Ignore
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 18baf6fa3ab837a82d725b72b8b60e3b33b7175f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444971"
---
# <a name="mofdeserializerschemavalidationoption-enumeration"></a><span data-ttu-id="43d90-103">MofDeserializerSchemaValidationOption-Enumeration</span><span class="sxs-lookup"><span data-stu-id="43d90-103">MofDeserializerSchemaValidationOption enumeration</span></span>

<span data-ttu-id="43d90-104">Definiert Konstanten, die Schemavalidierungsoptionen für die Deserialisierung angeben.</span><span class="sxs-lookup"><span data-stu-id="43d90-104">Defines constants that specify schema validation options for deserialization.</span></span>

<span data-ttu-id="43d90-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43d90-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="43d90-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="43d90-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="43d90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d90-107">Syntax</span></span>

``` csharp
internal enum MofDeserializerSchemaValidationOption
```

``` c++
private enum class MofDeserializerSchemaValidationOption
```

``` fsharp
type internal MofDeserializerSchemaValidationOption
```

``` vb
Friend Enumeration MofDeserializerSchemaValidationOption
```

## <a name="members"></a><span data-ttu-id="43d90-108">Member</span><span class="sxs-lookup"><span data-stu-id="43d90-108">Members</span></span>

|<span data-ttu-id="43d90-109">Membername</span><span class="sxs-lookup"><span data-stu-id="43d90-109">Member name</span></span>|<span data-ttu-id="43d90-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43d90-110">Description</span></span>|
|-|-|
|<span data-ttu-id="43d90-111">Standard</span><span class="sxs-lookup"><span data-stu-id="43d90-111">Default</span></span>|<span data-ttu-id="43d90-112">Gibt die Standardschemaüberprüfung an.</span><span class="sxs-lookup"><span data-stu-id="43d90-112">Specifies default schema validation.</span></span>|
|<span data-ttu-id="43d90-113">Strict</span><span class="sxs-lookup"><span data-stu-id="43d90-113">Strict</span></span>|<span data-ttu-id="43d90-114">Gibt die strenge Schemavalidierung an.</span><span class="sxs-lookup"><span data-stu-id="43d90-114">Specifies strict schema validation.</span></span>|
|<span data-ttu-id="43d90-115">Lose</span><span class="sxs-lookup"><span data-stu-id="43d90-115">Loose</span></span>|<span data-ttu-id="43d90-116">Gibt eine lose Schemavalidierung an.</span><span class="sxs-lookup"><span data-stu-id="43d90-116">Specifies loose schema validation.</span></span>|
|<span data-ttu-id="43d90-117">IgnorePropertyType</span><span class="sxs-lookup"><span data-stu-id="43d90-117">IgnorePropertyType</span></span>|<span data-ttu-id="43d90-118">Gibt an, dass die Schemavalidierung Eigenschaftstypen ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="43d90-118">Specifies that schema validation should ignore property types.</span></span>|
|<span data-ttu-id="43d90-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="43d90-119">Ignore</span></span>|<span data-ttu-id="43d90-120">Gibt an, dass die Schemavalidierung ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d90-120">Specifies that schema validation should be ignored.</span></span>|

## <a name="see-also"></a><span data-ttu-id="43d90-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43d90-121">See Also</span></span>

<span data-ttu-id="43d90-122">[Microsoft.Management.Infrastructure.Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43d90-122">[Microsoft.Management.Infrastructure.Serialization Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
