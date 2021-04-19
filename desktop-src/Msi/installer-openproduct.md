---
description: Die openproduct-Methode des Installer-Objekts öffnet mithilfe des Produktcodes ein Installationspaket für ein installiertes Produkt und gibt ein Session-Objekt zurück.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. openproduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359765"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="02395-103">Installer. openproduct-Methode</span><span class="sxs-lookup"><span data-stu-id="02395-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="02395-104">Die **openproduct** -Methode des [**Installer**](installer-object.md) -Objekts öffnet mithilfe des Produktcodes ein Installationspaket für ein installiertes Produkt und gibt ein [**Session**](session-object.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="02395-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02395-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02395-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="02395-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02395-107">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="02395-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="02395-108">Erforderliche Zeichenfolge, die den eindeutigen Produktcode (eine [GUID](guid.md)) oder einen vom Installer geschriebenen Aktivierungs Deskriptor enthält.</span><span class="sxs-lookup"><span data-stu-id="02395-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02395-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02395-109">Return value</span></span>

<span data-ttu-id="02395-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02395-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02395-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02395-111">Remarks</span></span>

<span data-ttu-id="02395-112">Beachten Sie, dass nur ein [**Sitzungs**](session-object.md) Objekt von einem einzelnen Prozess geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="02395-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="02395-113">**Openproduct** kann nicht in einer benutzerdefinierten Aktion verwendet werden, da die aktive Installation die einzige zulässige Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="02395-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="02395-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02395-114">Requirements</span></span>



| <span data-ttu-id="02395-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02395-115">Requirement</span></span> | <span data-ttu-id="02395-116">Wert</span><span class="sxs-lookup"><span data-stu-id="02395-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02395-117">Version</span><span class="sxs-lookup"><span data-stu-id="02395-117">Version</span></span><br/> | <span data-ttu-id="02395-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02395-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02395-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02395-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02395-120">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="02395-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="02395-121">DLL</span><span class="sxs-lookup"><span data-stu-id="02395-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="02395-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02395-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="02395-123">IID</span><span class="sxs-lookup"><span data-stu-id="02395-123">IID</span></span><br/>     | <span data-ttu-id="02395-124">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="02395-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




