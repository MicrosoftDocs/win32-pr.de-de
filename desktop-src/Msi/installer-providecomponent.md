---
description: Die providecomponent-Methode des Installer-Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer. providecomponent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371159"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="78c7d-103">Installer. providecomponent-Methode</span><span class="sxs-lookup"><span data-stu-id="78c7d-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="78c7d-104">Die **providecomponent** -Methode des [**Installer**](installer-object.md) -Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.</span><span class="sxs-lookup"><span data-stu-id="78c7d-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="78c7d-105">Bei Bedarf fordert die **providecomponent** -Methode des [**Installer**](installer-object.md) -Objekts zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.</span><span class="sxs-lookup"><span data-stu-id="78c7d-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c7d-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="78c7d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c7d-108">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="78c7d-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="78c7d-109">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="78c7d-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-110">*Feature*</span><span class="sxs-lookup"><span data-stu-id="78c7d-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="78c7d-111">Gibt die Funktions-ID der Funktion an, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="78c7d-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-112">*Komponente*</span><span class="sxs-lookup"><span data-stu-id="78c7d-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="78c7d-113">Gibt den Komponenten Code an.</span><span class="sxs-lookup"><span data-stu-id="78c7d-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="78c7d-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="78c7d-115">Definiert den Installationsmodus.</span><span class="sxs-lookup"><span data-stu-id="78c7d-115">Defines the installation mode.</span></span> <span data-ttu-id="78c7d-116">Dieser Parameter kann einer der Werte sein, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="78c7d-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="78c7d-117">Name</span><span class="sxs-lookup"><span data-stu-id="78c7d-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="78c7d-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="78c7d-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="78c7d-119"><dt>**msiinstallmodedefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="78c7d-120">Stellt den Komponenten Pfad bereit und führt ggf. eine beliebige Installation durch.</span><span class="sxs-lookup"><span data-stu-id="78c7d-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="78c7d-121"><dt>**msiinstallmodevorhandenes**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="78c7d-122">Gibt den Komponenten Pfad nur dann an, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78c7d-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="78c7d-123">Dieser Modus überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="78c7d-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="78c7d-124"><dt>**msiinstallmudenoerkennungs**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="78c7d-125">Gibt den Komponenten Pfad nur dann an, wenn das Feature vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="78c7d-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="78c7d-126">Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78c7d-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="78c7d-127">In diesem Modus wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="78c7d-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="78c7d-128"><dt>**msiinstallmudenosourceresolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="78c7d-129">Stellt den Komponenten Pfad nur dann bereit, wenn die Funktion mit einem InstallState-Parameter von *msiinstallstatelocal* vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="78c7d-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="78c7d-130">Dadurch wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="78c7d-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="78c7d-131"><dt>**Kombination der msireinstallmode-Flags**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="78c7d-132">Ruft [**reinstallfeature**](installer-reinstallfeature.md) auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* -Parameter erneut zu installieren, und stellt dann die Komponente bereit.</span><span class="sxs-lookup"><span data-stu-id="78c7d-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c7d-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78c7d-133">Return value</span></span>

<span data-ttu-id="78c7d-134">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78c7d-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78c7d-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78c7d-135">Remarks</span></span>

<span data-ttu-id="78c7d-136">Die **providecomponent** -Methode kombiniert die Funktionalität von [**usefeature**](installer-usefeature.md), [**Konfigurierung**](installer-configurefeature.md)und [**componentpath**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="78c7d-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="78c7d-137">Die **providecomponent** -Methode vereinfacht die Aufruf Sequenz, erhöht aber auch den Verwendungs Zähler und sollte mit Vorsicht verwendet werden, um eine ungenaue Verwendungs Anzahl zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="78c7d-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="78c7d-138">Die **providecomponent** -Methode bietet auch weniger Flexibilität als eine Reihe einzelner Aufrufe der bereits erwähnten Methoden und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="78c7d-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="78c7d-139">Wenn die Anwendung nach einer unerwarteten Situation wieder hergestellt wird, hat die Anwendung wahrscheinlich bereits [**usefeature**](installer-usefeature.md) aufgerufen und die Verwendungs Anzahl erhöht.</span><span class="sxs-lookup"><span data-stu-id="78c7d-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="78c7d-140">In diesem Fall sollte die Anwendung das Erhöhen der Verwendungs Anzahl vermeiden, indem anstelle der **providecomponent** -Methode die Methode " [**Konfigurierung**](installer-configurefeature.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="78c7d-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="78c7d-141">Die msiinstallmodevorhandene-Option kann nicht in Kombination mit msireinstallmode-Flags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78c7d-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c7d-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c7d-142">Requirements</span></span>



| <span data-ttu-id="78c7d-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78c7d-143">Requirement</span></span> | <span data-ttu-id="78c7d-144">Wert</span><span class="sxs-lookup"><span data-stu-id="78c7d-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c7d-145">Version</span><span class="sxs-lookup"><span data-stu-id="78c7d-145">Version</span></span><br/> | <span data-ttu-id="78c7d-146">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78c7d-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78c7d-147">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78c7d-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78c7d-148">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="78c7d-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="78c7d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="78c7d-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="78c7d-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="78c7d-151">IID</span><span class="sxs-lookup"><span data-stu-id="78c7d-151">IID</span></span><br/>     | <span data-ttu-id="78c7d-152">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="78c7d-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="78c7d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c7d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c7d-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="78c7d-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




