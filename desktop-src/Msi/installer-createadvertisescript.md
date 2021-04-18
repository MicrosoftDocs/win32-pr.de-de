---
description: Mit der Methode "-Methode" der Methode "-Installer" wird ein Ankündigungs Skript generiert.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Installer:: kreatewerbung-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358155"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="b7781-103">Installer:: kreatewerbung-Methode</span><span class="sxs-lookup"><span data-stu-id="b7781-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="b7781-104">Mit **der Methode "** -Methode" der Methode "- [**Installer**](installer-object.md) " wird ein Ankündigungs Skript generiert.</span><span class="sxs-lookup"><span data-stu-id="b7781-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7781-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7781-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="b7781-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7781-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="b7781-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-108">Der vollständige Pfad zum Windows Installer Paket (. msi), das angekündigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7781-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="b7781-109">*ScriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="b7781-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-110">Der vollständige Pfad zu der Skriptdatei, die mit den angekündigten Informationen erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7781-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="b7781-111">*Kranz*</span><span class="sxs-lookup"><span data-stu-id="b7781-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-112">Die Liste der Transformationen, die auf das Produkt angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7781-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="b7781-113">Transformationen in der Liste werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="b7781-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="b7781-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7781-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b7781-115">*language*</span><span class="sxs-lookup"><span data-stu-id="b7781-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-116">Die Sprache des zu verwendenden Installationspakets.</span><span class="sxs-lookup"><span data-stu-id="b7781-116">The language of the installation package to use.</span></span> <span data-ttu-id="b7781-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7781-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b7781-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="b7781-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-119">Dieser Parameter gibt an, für welche Plattform das Installationsprogramm vom Installationsprogramm erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7781-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="b7781-120">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="b7781-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b7781-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b7781-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="b7781-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7781-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="b7781-123"><dt>**msiankündigen-currentplatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="b7781-124">Erstellt ein Skript für die aktuelle Plattform.</span><span class="sxs-lookup"><span data-stu-id="b7781-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="b7781-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="b7781-126">Erstellt ein Skript für die x86-Plattform.</span><span class="sxs-lookup"><span data-stu-id="b7781-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="b7781-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="b7781-128">Erstellt ein Skript für Itanium-basierte Systeme.</span><span class="sxs-lookup"><span data-stu-id="b7781-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="b7781-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="b7781-130">Erstellt ein Skript für die x64-Plattform.</span><span class="sxs-lookup"><span data-stu-id="b7781-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="b7781-131">*options*</span><span class="sxs-lookup"><span data-stu-id="b7781-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="b7781-132">Ankündigungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="b7781-132">Advertisement options.</span></span> <span data-ttu-id="b7781-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7781-133">This parameter is optional.</span></span> <span data-ttu-id="b7781-134">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="b7781-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="b7781-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b7781-135">This parameter is optional.</span></span>



| <span data-ttu-id="b7781-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b7781-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="b7781-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7781-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="b7781-138"><dt>**msiankündigen-Standard**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="b7781-139">Standard Ankündigung</span><span class="sxs-lookup"><span data-stu-id="b7781-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="b7781-140"><dt>**msiwerbesesinglabstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b7781-141">Gibt eine neue Instanz des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b7781-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="b7781-142">Erfordert, dass die erste Transformation in der Transformations Liste des *Transformationen* -Parameters die instanztransformation ist, mit der der Produktcode geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b7781-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="b7781-143">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="b7781-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7781-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7781-144">Return value</span></span>

<span data-ttu-id="b7781-145">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b7781-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7781-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7781-146">Remarks</span></span>

<span data-ttu-id="b7781-147">Die [**Methode "**](installer-advertiseproduct.md) ankündigen" verwendet die [**msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b7781-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="b7781-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7781-148">Examples</span></span>

<span data-ttu-id="b7781-149">Im folgenden Beispiel wird die Verwendung der Methode " **kreatewerbung** " veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b7781-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="b7781-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7781-150">Requirements</span></span>



| <span data-ttu-id="b7781-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7781-151">Requirement</span></span> | <span data-ttu-id="b7781-152">Wert</span><span class="sxs-lookup"><span data-stu-id="b7781-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7781-153">Version</span><span class="sxs-lookup"><span data-stu-id="b7781-153">Version</span></span><br/> | <span data-ttu-id="b7781-154">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7781-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7781-155">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7781-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7781-156">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7781-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="b7781-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b7781-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="b7781-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7781-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="b7781-159">IID</span><span class="sxs-lookup"><span data-stu-id="b7781-159">IID</span></span><br/>     | <span data-ttu-id="b7781-160">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b7781-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="b7781-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7781-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7781-162">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="b7781-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="b7781-163">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7781-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




