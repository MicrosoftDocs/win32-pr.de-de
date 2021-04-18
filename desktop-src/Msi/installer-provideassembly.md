---
description: Die ProvideAssembly-Methode des Installer-Objekts gibt den installierten Pfad einer Assembly zurück.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Installer::P rovideassembly-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371300"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="f9c78-103">Installer::P rovideassembly-Methode</span><span class="sxs-lookup"><span data-stu-id="f9c78-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="f9c78-104">Die **ProvideAssembly** -Methode des [**Installer**](installer-object.md) -Objekts gibt den installierten Pfad einer Assembly zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c78-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9c78-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="f9c78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c78-107">*Stadtverordneten*</span><span class="sxs-lookup"><span data-stu-id="f9c78-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c78-108">Der starke Name der installierten Assembly, die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9c78-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="f9c78-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="f9c78-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c78-110">Legen Sie für globale Assemblys auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="f9c78-110">Set to null for global assemblies.</span></span> <span data-ttu-id="f9c78-111">Legen Sie für private Assemblys *appContext* auf den vollständigen Pfad der Anwendungs Konfigurationsdatei oder auf den vollständigen Pfad der ausführbaren Datei der Anwendung fest, in der die Assembly als privat erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9c78-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="f9c78-112">*' installmode '*</span><span class="sxs-lookup"><span data-stu-id="f9c78-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c78-113">Definiert den Installationsmodus.</span><span class="sxs-lookup"><span data-stu-id="f9c78-113">Defines the installation mode.</span></span> <span data-ttu-id="f9c78-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f9c78-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f9c78-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c78-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="f9c78-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9c78-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="f9c78-117"><dt>**msiinstallmodedefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="f9c78-118">Geben Sie die Komponente an, und führen Sie jede erforderliche Installation aus, um die Komponente bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="f9c78-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="f9c78-119"><dt>**msiinstallmodevorhandenes**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="f9c78-120">Geben Sie die Komponente nur dann an, wenn das Feature vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f9c78-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="f9c78-121">Mit dieser Option wird überprüft, ob die Assembly vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f9c78-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="f9c78-122"><dt>**msiinstallmudenoerkennungs**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="f9c78-123">Geben Sie die Komponente nur dann an, wenn das Feature vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f9c78-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="f9c78-124">Mit dieser Option wird nicht überprüft, ob die Assembly vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f9c78-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="f9c78-125"><dt>**msiinstallmudenosourceresolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="f9c78-126">Stellt die Assembly nur dann bereit, wenn die Assembly lokal installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9c78-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="f9c78-127"><dt>**Kombination der von [ **reinstallfeature** verwendeten Flags](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="f9c78-128">Ruft die [**reinstallfeature**](installer-reinstallfeature.md) -Methode auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* erneut zu installieren, und gibt dann den Assemblypfad zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c78-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f9c78-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="f9c78-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c78-130">Assemblyinformationen und Assemblytyp.</span><span class="sxs-lookup"><span data-stu-id="f9c78-130">Assembly information and assembly type.</span></span> <span data-ttu-id="f9c78-131">Legen Sie auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="f9c78-131">Set to one of the following values.</span></span>



| <span data-ttu-id="f9c78-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c78-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="f9c78-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f9c78-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="f9c78-134"><dt>**msiprovide assemblynet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="f9c78-135">Eine .NET-Assembly.</span><span class="sxs-lookup"><span data-stu-id="f9c78-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="f9c78-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f9c78-137">Eine parallele Win32-Assembly.</span><span class="sxs-lookup"><span data-stu-id="f9c78-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c78-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9c78-138">Return value</span></span>

<span data-ttu-id="f9c78-139">Der Pfad zur installierten Assembly.</span><span class="sxs-lookup"><span data-stu-id="f9c78-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c78-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9c78-140">Remarks</span></span>

<span data-ttu-id="f9c78-141">Die **ProvideAssembly** -Methode verwendet die [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f9c78-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="f9c78-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9c78-142">Examples</span></span>

<span data-ttu-id="f9c78-143">Im folgenden Beispielskript wird die Verwendung der ProvideAssembly-Methode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f9c78-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="f9c78-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9c78-144">Requirements</span></span>



| <span data-ttu-id="f9c78-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9c78-145">Requirement</span></span> | <span data-ttu-id="f9c78-146">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c78-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c78-147">Version</span><span class="sxs-lookup"><span data-stu-id="f9c78-147">Version</span></span><br/> | <span data-ttu-id="f9c78-148">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9c78-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f9c78-149">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9c78-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f9c78-150">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9c78-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="f9c78-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c78-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9c78-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c78-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="f9c78-153">IID</span><span class="sxs-lookup"><span data-stu-id="f9c78-153">IID</span></span><br/>     | <span data-ttu-id="f9c78-154">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f9c78-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="f9c78-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9c78-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c78-156">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="f9c78-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="f9c78-157">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9c78-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




