---
description: Die fileversion-Methode des Installer-Objekts gibt die Versions Zeichenfolge oder die sprach Zeichenfolge des Pfads zurück, der im Pfad unter Verwendung des Formats angegeben ist, in dem das Installationsprogramm diese in der Datenbank finden soll
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370519"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="114f3-103">Installer. FileVersion-Methode</span><span class="sxs-lookup"><span data-stu-id="114f3-103">Installer.FileVersion method</span></span>

<span data-ttu-id="114f3-104">Die **fileversion** -Methode des [**Installer**](installer-object.md) -Objekts gibt die Versions Zeichenfolge oder die sprach Zeichenfolge des Pfads zurück, der im *Pfad* unter Verwendung des Formats angegeben ist, in dem das Installationsprogramm diese in der Datenbank finden soll</span><span class="sxs-lookup"><span data-stu-id="114f3-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="114f3-105">Bei Versionen ist dies eine Zeichenfolge im \# Format ". \# . \# . \# ".</span><span class="sxs-lookup"><span data-stu-id="114f3-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="114f3-106">In der Sprache ist dies die dezimale Sprach-ID.</span><span class="sxs-lookup"><span data-stu-id="114f3-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="114f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="114f3-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="114f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="114f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114f3-109">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="114f3-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="114f3-110">Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="114f3-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="114f3-111">*Sprache*</span><span class="sxs-lookup"><span data-stu-id="114f3-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="114f3-112">Flag zum Festlegen, ob der zurückgegebene Wert eine Sprach-ID oder eine Versions Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="114f3-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="114f3-113">TRUE gibt die Sprache zurück, false gibt die Version zurück.</span><span class="sxs-lookup"><span data-stu-id="114f3-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="114f3-114">Dieser Parameter ist optional, und der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="114f3-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114f3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="114f3-115">Return value</span></span>

<span data-ttu-id="114f3-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="114f3-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="114f3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="114f3-117">Requirements</span></span>



| <span data-ttu-id="114f3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="114f3-118">Requirement</span></span> | <span data-ttu-id="114f3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="114f3-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114f3-120">Version</span><span class="sxs-lookup"><span data-stu-id="114f3-120">Version</span></span><br/> | <span data-ttu-id="114f3-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="114f3-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="114f3-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="114f3-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="114f3-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="114f3-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="114f3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="114f3-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="114f3-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="114f3-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="114f3-126">IID</span><span class="sxs-lookup"><span data-stu-id="114f3-126">IID</span></span><br/>     | <span data-ttu-id="114f3-127">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="114f3-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




