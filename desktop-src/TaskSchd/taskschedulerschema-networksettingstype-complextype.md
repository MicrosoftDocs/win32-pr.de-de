---
title: komplexer networksettingstype-Typ
description: Definiert die Elemente, die die Einstellungen bereitstellen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- komplexer networksettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956682"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="cedf8-104">komplexer networksettingstype-Typ</span><span class="sxs-lookup"><span data-stu-id="cedf8-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="cedf8-105">Definiert die Elemente, die die Einstellungen bereitstellen, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cedf8-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cedf8-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cedf8-106">Child elements</span></span>



| <span data-ttu-id="cedf8-107">Element</span><span class="sxs-lookup"><span data-stu-id="cedf8-107">Element</span></span>                                                              | <span data-ttu-id="cedf8-108">type</span><span class="sxs-lookup"><span data-stu-id="cedf8-108">Type</span></span>                                                        | <span data-ttu-id="cedf8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cedf8-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cedf8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="cedf8-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="cedf8-111">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="cedf8-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="cedf8-112">Gibt einen GUID-Wert an, der ein Netzwerk Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cedf8-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="cedf8-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="cedf8-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="cedf8-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="cedf8-114">nonEmptyString</span></span>                                              | <span data-ttu-id="cedf8-115">Gibt den Namen eines Netzwerk Profils an.</span><span class="sxs-lookup"><span data-stu-id="cedf8-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="cedf8-116">Der Name wird zu Anzeige Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="cedf8-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cedf8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cedf8-117">Requirements</span></span>



| <span data-ttu-id="cedf8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cedf8-118">Requirement</span></span> | <span data-ttu-id="cedf8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cedf8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cedf8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cedf8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cedf8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cedf8-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cedf8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cedf8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cedf8-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cedf8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





