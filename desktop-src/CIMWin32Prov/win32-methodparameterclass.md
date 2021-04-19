---
description: Die \_ WMI-Basisklasse "Win32 methodparameterclass abstract" leitet eine beliebige Klasse ab, die als Container von Parameterwerten definiert ist, die an eine Methode übergeben werden.
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Win32_MethodParameterClass-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346008"
---
# <a name="win32_methodparameterclass-class"></a><span data-ttu-id="f8d1f-103">Win32 \_ methodparameterclass-Klasse</span><span class="sxs-lookup"><span data-stu-id="f8d1f-103">Win32\_MethodParameterClass class</span></span>

<span data-ttu-id="f8d1f-104">Die [WMI](/windows/desktop/WmiSdk/retrieving-a-class) -Basisklasse " **Win32 \_ methodparameterclass** abstract" leitet eine beliebige Klasse ab, die als Container von Parameterwerten definiert ist, die an eine Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8d1f-104">The **Win32\_MethodParameterClass** abstract, base [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) derives any class defined as a container of parameter values that will be passed to a method.</span></span> <span data-ttu-id="f8d1f-105">Diese Klasse dient als Klassifizierungs Knoten und besitzt keine eigenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8d1f-105">Having no properties of its own, this class serves as a classification node.</span></span> <span data-ttu-id="f8d1f-106">Ein ähnliches Beispiel ist [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8d1f-106">A similar example is [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span> <span data-ttu-id="f8d1f-107">Ableitung von **CIM \_ PhysicalElement** gibt an, dass die Klasse eine physische anstelle einer logischen Entität beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f8d1f-107">Derivation from **CIM\_PhysicalElement** indicates that the class describes a physical rather than logical entity.</span></span> <span data-ttu-id="f8d1f-108">Im Fall von **Win32 \_ methodparameterclass** werden Klassen, die von dieser abgeleitet werden, speziell erstellt, um Parameter an eine Methode zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f8d1f-108">In the case of **Win32\_MethodParameterClass**, classes derived from it are created specifically to pass parameters to a method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8d1f-109">Syntax</span></span>

## <a name="members"></a><span data-ttu-id="f8d1f-110">Member</span><span class="sxs-lookup"><span data-stu-id="f8d1f-110">Members</span></span>

<span data-ttu-id="f8d1f-111">Die **Win32 \_ methodparameterclass** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="f8d1f-111">The **Win32\_MethodParameterClass** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d1f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8d1f-112">Requirements</span></span>



| <span data-ttu-id="f8d1f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8d1f-113">Requirement</span></span> | <span data-ttu-id="f8d1f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f8d1f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d1f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8d1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d1f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8d1f-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8d1f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8d1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d1f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8d1f-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8d1f-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8d1f-119">Namespace</span></span><br/>                | <span data-ttu-id="f8d1f-120">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f8d1f-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8d1f-121">MOF</span><span class="sxs-lookup"><span data-stu-id="f8d1f-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8d1f-122"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f8d1f-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8d1f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f8d1f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8d1f-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8d1f-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8d1f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8d1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d1f-126">WMI-Dienst Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="f8d1f-126">WMI Service Management Classes</span></span>](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

