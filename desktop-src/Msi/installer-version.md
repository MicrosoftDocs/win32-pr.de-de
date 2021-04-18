---
description: Die Version-Eigenschaft des Installer-Objekts ist eine schreibgeschützte Eigenschaft, die die Zeichen folgen Darstellung der aktuellen Version von Windows Installer darstellt. Die Zeichenfolge wird in der folgenden Form zurückgegeben.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Installer. Version (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372449"
---
# <a name="installerversion-property"></a><span data-ttu-id="a3e61-104">Installer. Version (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a3e61-104">Installer.Version property</span></span>

<span data-ttu-id="a3e61-105">Die **Version** -Eigenschaft des [**Installer**](installer-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die die Zeichen folgen Darstellung der aktuellen Version von Windows Installer darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3e61-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="a3e61-106">Die Zeichenfolge wird in der folgenden Form zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a3e61-106">The string is returned in the following form.</span></span>

<span data-ttu-id="a3e61-107">*Haupt* Version. *neben* Version. *Erstellen* Sie. *Aktualisieren*</span><span class="sxs-lookup"><span data-stu-id="a3e61-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="a3e61-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a3e61-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e61-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3e61-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="a3e61-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a3e61-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e61-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3e61-111">Requirements</span></span>



| <span data-ttu-id="a3e61-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3e61-112">Requirement</span></span> | <span data-ttu-id="a3e61-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a3e61-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e61-114">Version</span><span class="sxs-lookup"><span data-stu-id="a3e61-114">Version</span></span><br/> | <span data-ttu-id="a3e61-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3e61-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a3e61-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3e61-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a3e61-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3e61-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a3e61-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e61-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3e61-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e61-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a3e61-120">IID</span><span class="sxs-lookup"><span data-stu-id="a3e61-120">IID</span></span><br/>     | <span data-ttu-id="a3e61-121">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a3e61-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




