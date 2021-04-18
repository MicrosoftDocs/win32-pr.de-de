---
description: Die forcesourcelistresolution-Methode des Installer-Objekts erzwingt das Windows Installer, die Quell Liste nach einer gültigen Produkt Quelle zu durchsuchen.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. forcesourcelistresolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364789"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="e2d0e-103">Installer. forcesourcelistresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="e2d0e-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="e2d0e-104">Die **forcesourcelistresolution** -Methode des [**Installer**](installer-object.md) -Objekts erzwingt, dass das Installationsprogramm die Quell Liste nach einer gültigen Produkt Quelle durchsucht, wenn eine Quelle das nächste Mal benötigt wird, z. b. wenn das Installationsprogramm eine Installation oder eine Neuinstallation ausführt oder wenn der Pfad für die Ausführung einer Komponente von der Quelle benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2d0e-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="e2d0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d0e-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="e2d0e-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d0e-108">Gibt den Produktcode an.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="e2d0e-109">*Benutzer*</span><span class="sxs-lookup"><span data-stu-id="e2d0e-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d0e-110">Benutzername für die Installation pro Benutzer NULL oder eine leere Zeichenfolge für die Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d0e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2d0e-111">Return value</span></span>

<span data-ttu-id="e2d0e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d0e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2d0e-113">Requirements</span></span>



| <span data-ttu-id="e2d0e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2d0e-114">Requirement</span></span> | <span data-ttu-id="e2d0e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e2d0e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d0e-116">Version</span><span class="sxs-lookup"><span data-stu-id="e2d0e-116">Version</span></span><br/> | <span data-ttu-id="e2d0e-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2d0e-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2d0e-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2d0e-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2d0e-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e2d0e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e2d0e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2d0e-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d0e-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e2d0e-122">IID</span><span class="sxs-lookup"><span data-stu-id="e2d0e-122">IID</span></span><br/>     | <span data-ttu-id="e2d0e-123">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e2d0e-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e2d0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2d0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d0e-125">**Msisourcelistforceresolution**</span><span class="sxs-lookup"><span data-stu-id="e2d0e-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="e2d0e-126">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="e2d0e-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




