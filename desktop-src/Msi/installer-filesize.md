---
description: Die Filesize-Methode des Installer-Objekts verwendet Win32-API-Aufrufe, um die Größe der in path angegebenen Datei zurückzugeben.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. Filesize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369551"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="71ca4-103">Installer. Filesize-Methode</span><span class="sxs-lookup"><span data-stu-id="71ca4-103">Installer.FileSize method</span></span>

<span data-ttu-id="71ca4-104">Die **FileSize** -Methode des [**Installer**](installer-object.md) -Objekts verwendet Win32-API-Aufrufe, um die Größe der in *path* angegebenen Datei zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="71ca4-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ca4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ca4-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="71ca4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ca4-107">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="71ca4-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="71ca4-108">Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="71ca4-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ca4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71ca4-109">Return value</span></span>

<span data-ttu-id="71ca4-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71ca4-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ca4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71ca4-111">Requirements</span></span>



| <span data-ttu-id="71ca4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71ca4-112">Requirement</span></span> | <span data-ttu-id="71ca4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="71ca4-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ca4-114">Version</span><span class="sxs-lookup"><span data-stu-id="71ca4-114">Version</span></span><br/> | <span data-ttu-id="71ca4-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71ca4-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="71ca4-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71ca4-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="71ca4-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="71ca4-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="71ca4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="71ca4-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="71ca4-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ca4-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="71ca4-120">IID</span><span class="sxs-lookup"><span data-stu-id="71ca4-120">IID</span></span><br/>     | <span data-ttu-id="71ca4-121">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="71ca4-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




