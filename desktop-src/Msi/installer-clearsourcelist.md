---
description: Mit der clearsourcelist-Methode des Installer-Objekts werden alle Netzwerk Quellen aus der Quell Liste entfernt.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer. clearsourcelist-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366026"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="c1277-103">Installer. clearsourcelist-Methode</span><span class="sxs-lookup"><span data-stu-id="c1277-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="c1277-104">Mit der **clearsourcelist** -Methode des [**Installer**](installer-object.md) -Objekts werden alle Netzwerk Quellen aus der Quell Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1277-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1277-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1277-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="c1277-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1277-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1277-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="c1277-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="c1277-108">Gibt den Produktcode an.</span><span class="sxs-lookup"><span data-stu-id="c1277-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="c1277-109">*Benutzer*</span><span class="sxs-lookup"><span data-stu-id="c1277-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="c1277-110">Benutzername für die Installation pro Benutzer NULL oder eine leere Zeichenfolge für die Installation pro Computer.</span><span class="sxs-lookup"><span data-stu-id="c1277-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1277-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1277-111">Return value</span></span>

<span data-ttu-id="c1277-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c1277-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1277-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1277-113">Requirements</span></span>



| <span data-ttu-id="c1277-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1277-114">Requirement</span></span> | <span data-ttu-id="c1277-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c1277-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1277-116">Version</span><span class="sxs-lookup"><span data-stu-id="c1277-116">Version</span></span><br/> | <span data-ttu-id="c1277-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1277-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1277-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1277-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1277-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1277-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c1277-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c1277-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1277-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1277-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c1277-122">IID</span><span class="sxs-lookup"><span data-stu-id="c1277-122">IID</span></span><br/>     | <span data-ttu-id="c1277-123">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c1277-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c1277-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1277-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1277-125">**Msisourcelistclearall**</span><span class="sxs-lookup"><span data-stu-id="c1277-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="c1277-126">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="c1277-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




