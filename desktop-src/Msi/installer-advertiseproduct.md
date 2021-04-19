---
description: Mit der "ankündigen"-Methode des Installerobjekts wird ein Installationspaket angekündigt.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Installer:: ankündigen-Product-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369715"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="15696-103">Installer:: ankündigen-Product-Methode</span><span class="sxs-lookup"><span data-stu-id="15696-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="15696-104">Mit der "ankündigen" **-Methode des** [**Installerobjekts**](installer-object.md) wird ein Installationspaket angekündigt.</span><span class="sxs-lookup"><span data-stu-id="15696-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="15696-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15696-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="15696-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15696-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="15696-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="15696-108">Der vollständige Pfad zum Windows Installer Paket (. msi), das angekündigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="15696-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="15696-109">*context*</span><span class="sxs-lookup"><span data-stu-id="15696-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="15696-110">Der Kontext der Ankündigung.</span><span class="sxs-lookup"><span data-stu-id="15696-110">The context of the advertisement.</span></span> <span data-ttu-id="15696-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="15696-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="15696-112">Wert</span><span class="sxs-lookup"><span data-stu-id="15696-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="15696-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="15696-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="15696-114"><dt>**msiankündigen-productmachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="15696-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="15696-115">Kündigt die Anwendung für eine [Installation im Installations Kontext](installation-context.md)pro Computer an.</span><span class="sxs-lookup"><span data-stu-id="15696-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="15696-116">Dadurch wird das Paket für die Installation durch alle Benutzer des Computers zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="15696-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="15696-117"><dt>**msiankündigen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="15696-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="15696-118">Kündigt die Anwendung für eine Installation im [Installations Kontext](installation-context.md)pro Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="15696-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="15696-119">*Kranz*</span><span class="sxs-lookup"><span data-stu-id="15696-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="15696-120">Die Liste der Transformationen, die auf das Produkt angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15696-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="15696-121">Transformationen in der Liste werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="15696-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="15696-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="15696-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="15696-123">*language*</span><span class="sxs-lookup"><span data-stu-id="15696-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="15696-124">Die Sprache des zu verwendenden Installationspakets.</span><span class="sxs-lookup"><span data-stu-id="15696-124">The language of the installation package to use.</span></span> <span data-ttu-id="15696-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="15696-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="15696-126">*options*</span><span class="sxs-lookup"><span data-stu-id="15696-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="15696-127">Die Ankündigungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="15696-127">The advertisement options.</span></span> <span data-ttu-id="15696-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="15696-128">This parameter is optional.</span></span> <span data-ttu-id="15696-129">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="15696-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="15696-130">Wert</span><span class="sxs-lookup"><span data-stu-id="15696-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="15696-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="15696-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="15696-132"><dt>**msiankündigen-Standard**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="15696-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="15696-133">Standard Ankündigung</span><span class="sxs-lookup"><span data-stu-id="15696-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="15696-134"><dt>**msiwerbesesinglabstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="15696-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="15696-135">Gibt eine neue Instanz des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="15696-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="15696-136">Erfordert, dass die erste Transformation in der Transformations Liste des *Transformationen* -Parameters die instanztransformation ist, mit der der Produktcode geändert wird.</span><span class="sxs-lookup"><span data-stu-id="15696-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="15696-137">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="15696-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15696-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15696-138">Return value</span></span>

<span data-ttu-id="15696-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="15696-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15696-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15696-140">Remarks</span></span>

<span data-ttu-id="15696-141">Die **Methode "** ankündigen" verwendet die [**msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="15696-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="15696-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15696-142">Examples</span></span>

<span data-ttu-id="15696-143">Im folgenden Beispiel wird die Verwendung der-Methode von " **Werbung** " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="15696-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="15696-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15696-144">Requirements</span></span>



| <span data-ttu-id="15696-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15696-145">Requirement</span></span> | <span data-ttu-id="15696-146">Wert</span><span class="sxs-lookup"><span data-stu-id="15696-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15696-147">Version</span><span class="sxs-lookup"><span data-stu-id="15696-147">Version</span></span><br/> | <span data-ttu-id="15696-148">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15696-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15696-149">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15696-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15696-150">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="15696-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="15696-151">DLL</span><span class="sxs-lookup"><span data-stu-id="15696-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="15696-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15696-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="15696-153">IID</span><span class="sxs-lookup"><span data-stu-id="15696-153">IID</span></span><br/>     | <span data-ttu-id="15696-154">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="15696-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="15696-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15696-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15696-156">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="15696-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="15696-157">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15696-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




