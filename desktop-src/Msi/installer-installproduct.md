---
description: Mit der installproduct-Methode des Installer-Objekts wird ein Installer-Paket geöffnet und eine Installationssitzung initialisiert.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. installproduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355890"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="b5174-103">Installer. installproduct-Methode</span><span class="sxs-lookup"><span data-stu-id="b5174-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="b5174-104">Mit der **installproduct** -Methode des [**Installer**](installer-object.md) -Objekts wird ein Installer-Paket geöffnet und eine Installationssitzung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="b5174-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5174-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5174-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="b5174-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5174-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="b5174-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="b5174-108">Erforderliche Zeichenfolge, die den Pfad zum Installationspaket enthält.</span><span class="sxs-lookup"><span data-stu-id="b5174-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="b5174-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="b5174-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="b5174-110">Optionale Zeichenfolge, die Eigenschaft = Wert-Paare enthält, getrennt durch Leerraum.</span><span class="sxs-lookup"><span data-stu-id="b5174-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="b5174-111">Um eine administrative Installation auszuführen, schließen Sie action = admin in *propertyValues* ein.</span><span class="sxs-lookup"><span data-stu-id="b5174-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="b5174-112">Weitere Informationen finden Sie unter der [**Action**](action.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b5174-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5174-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5174-113">Return value</span></span>

<span data-ttu-id="b5174-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5174-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5174-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5174-115">Remarks</span></span>

<span data-ttu-id="b5174-116">Wenn Sie ein Produkt vollständig entfernen möchten, legen Sie Remove = All in *propertyValues* fest.</span><span class="sxs-lookup"><span data-stu-id="b5174-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="b5174-117">Weitere Informationen finden Sie unter [**Remove**](remove.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b5174-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5174-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5174-118">Requirements</span></span>



| <span data-ttu-id="b5174-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5174-119">Requirement</span></span> | <span data-ttu-id="b5174-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b5174-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5174-121">Version</span><span class="sxs-lookup"><span data-stu-id="b5174-121">Version</span></span><br/> | <span data-ttu-id="b5174-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5174-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b5174-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5174-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b5174-124">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5174-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b5174-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5174-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5174-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5174-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b5174-127">IID</span><span class="sxs-lookup"><span data-stu-id="b5174-127">IID</span></span><br/>     | <span data-ttu-id="b5174-128">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b5174-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




