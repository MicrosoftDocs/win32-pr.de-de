---
description: Die Environment-Eigenschaft des Installer-Objekts ist eine Lese-/Schreibeigenschaft, die der Zeichen folgen Wert für eine Umgebungsvariable des aktuellen Prozesses ist.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer. Environment (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350776"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="cf814-103">Installer. Environment (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cf814-103">Installer.Environment property</span></span>

<span data-ttu-id="cf814-104">Die **Environment** -Eigenschaft des [**Installer**](installer-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die der Zeichen folgen Wert für eine Umgebungsvariable des aktuellen Prozesses ist.</span><span class="sxs-lookup"><span data-stu-id="cf814-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="cf814-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cf814-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf814-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf814-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="cf814-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cf814-107">Property value</span></span>

<span data-ttu-id="cf814-108">Der Name der Umgebungsvariablen, die gelesen oder geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf814-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="cf814-109">Dabei wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="cf814-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf814-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf814-110">Remarks</span></span>

<span data-ttu-id="cf814-111">Das Festlegen einer Umgebungsvariablen mit der- **Umgebungs** Eigenschaft wirkt sich nur auf die aktive Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="cf814-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="cf814-112">Wenn Sie persistente Änderungen an einer Umgebungsvariablen vornehmen möchten, verwenden Sie die [Umgebungs Tabelle](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="cf814-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf814-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf814-113">Requirements</span></span>



| <span data-ttu-id="cf814-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf814-114">Requirement</span></span> | <span data-ttu-id="cf814-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cf814-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf814-116">Version</span><span class="sxs-lookup"><span data-stu-id="cf814-116">Version</span></span><br/> | <span data-ttu-id="cf814-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cf814-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cf814-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf814-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cf814-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf814-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cf814-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cf814-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf814-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf814-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cf814-122">IID</span><span class="sxs-lookup"><span data-stu-id="cf814-122">IID</span></span><br/>     | <span data-ttu-id="cf814-123">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cf814-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




