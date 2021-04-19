---
description: Das Abhängigkeits Objekt gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installations Datenbank zusammengeführt wurde.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Abhängigkeits Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359399"
---
# <a name="dependency-object"></a><span data-ttu-id="122bd-103">Abhängigkeitsobjekt</span><span class="sxs-lookup"><span data-stu-id="122bd-103">Dependency object</span></span>

<span data-ttu-id="122bd-104">Das **Abhängigkeits** Objekt gibt ein Modul zurück, von dem das aktuelle Modul abhängig ist und das noch nicht mit der aktuellen Installations Datenbank zusammengeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="122bd-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="122bd-105">Member</span><span class="sxs-lookup"><span data-stu-id="122bd-105">Members</span></span>

<span data-ttu-id="122bd-106">Das **Abhängigkeits** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="122bd-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="122bd-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="122bd-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="122bd-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="122bd-108">Properties</span></span>

<span data-ttu-id="122bd-109">Das **Abhängigkeits** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="122bd-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="122bd-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="122bd-110">Property</span></span>                                           | <span data-ttu-id="122bd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="122bd-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="122bd-112">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="122bd-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="122bd-113">Gibt die Sprache des Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="122bd-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="122bd-114">**Modul**</span><span class="sxs-lookup"><span data-stu-id="122bd-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="122bd-115">Gibt die Modul-ID des erforderlichen Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="122bd-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="122bd-116">**Version**</span><span class="sxs-lookup"><span data-stu-id="122bd-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="122bd-117">Gibt die Version des erforderlichen Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="122bd-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="122bd-118">C++</span><span class="sxs-lookup"><span data-stu-id="122bd-118">C++</span></span>

<span data-ttu-id="122bd-119">Schnittstelle **imsmdependenz: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="122bd-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="122bd-120">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="122bd-120">Interface ID</span></span>



| <span data-ttu-id="122bd-121">Konstante</span><span class="sxs-lookup"><span data-stu-id="122bd-121">Constant</span></span>                | <span data-ttu-id="122bd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="122bd-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="122bd-123">**IID \_ imsmabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="122bd-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="122bd-124">{0adda82d-2c26-11d2-Ad65-00a0c9af11a6}</span><span class="sxs-lookup"><span data-stu-id="122bd-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="122bd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="122bd-125">Requirements</span></span>



| <span data-ttu-id="122bd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="122bd-126">Requirement</span></span> | <span data-ttu-id="122bd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="122bd-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="122bd-128">Version</span><span class="sxs-lookup"><span data-stu-id="122bd-128">Version</span></span><br/> | <span data-ttu-id="122bd-129">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="122bd-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="122bd-130">Header</span><span class="sxs-lookup"><span data-stu-id="122bd-130">Header</span></span><br/>  | <dl> <span data-ttu-id="122bd-131"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="122bd-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="122bd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="122bd-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="122bd-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="122bd-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




