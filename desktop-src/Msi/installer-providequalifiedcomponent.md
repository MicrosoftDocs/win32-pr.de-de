---
description: Die providequalifiedcomponent-Methode des Installer-Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus. Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. providequalifiedcomponent-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357721"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="af9ab-104">Installer. providequalifiedcomponent-Methode</span><span class="sxs-lookup"><span data-stu-id="af9ab-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="af9ab-105">Die **providequalifiedcomponent** -Methode des [**Installer**](installer-object.md) -Objekts gibt den vollständigen Komponenten Pfad zurück und führt jede erforderliche Installation aus.</span><span class="sxs-lookup"><span data-stu-id="af9ab-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="af9ab-106">Bei Bedarf fordert diese Methode zur Eingabe der Quelle auf und erhöht den Verwendungs Zähler für das Feature.</span><span class="sxs-lookup"><span data-stu-id="af9ab-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af9ab-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="af9ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af9ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9ab-109">*Kategorie*</span><span class="sxs-lookup"><span data-stu-id="af9ab-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="af9ab-110">Gibt die Komponenten-ID für die angeforderte Komponente an.</span><span class="sxs-lookup"><span data-stu-id="af9ab-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="af9ab-111">Dies ist möglicherweise nicht die GUID für die Komponente selbst, sondern ein Server, der die richtige Funktionalität bereitstellt, wie in der Spalte ComponentID der [Tabelle PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="af9ab-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="af9ab-112">*Qualifizierer*</span><span class="sxs-lookup"><span data-stu-id="af9ab-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="af9ab-113">Gibt einen Qualifizierer in einer Liste von werbekomponenten an (aus der [PublishComponent-Tabelle](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="af9ab-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="af9ab-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="af9ab-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="af9ab-115">Definiert den Installationsmodus.</span><span class="sxs-lookup"><span data-stu-id="af9ab-115">Defines the installation mode.</span></span> <span data-ttu-id="af9ab-116">Dieser Parameter kann einer der Werte sein, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="af9ab-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="af9ab-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="af9ab-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="af9ab-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af9ab-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="af9ab-119"><dt>**msiinstallmodedefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="af9ab-120">Stellt die-Komponente bereit und führt jede erforderliche Installation aus.</span><span class="sxs-lookup"><span data-stu-id="af9ab-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="af9ab-121"><dt>**msiinstallmodevorhandenes**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="af9ab-122">Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af9ab-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="af9ab-123">Dieser Modus überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af9ab-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="af9ab-124"><dt>**msiinstallmudenoerkennungs**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="af9ab-125">Stellt die Komponente nur bereit, wenn das Feature vorhanden ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af9ab-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="af9ab-126">In diesem Modus wird nur überprüft, ob die Komponente registriert ist, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af9ab-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="af9ab-127"><dt>**msiinstallmudenosourceresolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="af9ab-128">Stellt den Komponenten Pfad nur dann bereit, wenn die Funktion mit einem InstallState-Parameter von *msiinstallstatelocal* vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af9ab-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="af9ab-129">Dadurch wird die Registrierung der Komponente überprüft, aber es wird nicht überprüft, ob die Schlüsseldatei der Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af9ab-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="af9ab-130"><dt>**Kombination der msireinstallmode-Flags**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="af9ab-131">Ruft [**reinstallfeature**](installer-reinstallfeature.md) auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* -Parameter erneut zu installieren, und stellt dann die Komponente bereit.</span><span class="sxs-lookup"><span data-stu-id="af9ab-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9ab-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af9ab-132">Return value</span></span>

<span data-ttu-id="af9ab-133">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="af9ab-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9ab-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af9ab-134">Requirements</span></span>



| <span data-ttu-id="af9ab-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af9ab-135">Requirement</span></span> | <span data-ttu-id="af9ab-136">Wert</span><span class="sxs-lookup"><span data-stu-id="af9ab-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9ab-137">Version</span><span class="sxs-lookup"><span data-stu-id="af9ab-137">Version</span></span><br/> | <span data-ttu-id="af9ab-138">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af9ab-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="af9ab-139">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="af9ab-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="af9ab-140">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="af9ab-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="af9ab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="af9ab-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="af9ab-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af9ab-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="af9ab-143">IID</span><span class="sxs-lookup"><span data-stu-id="af9ab-143">IID</span></span><br/>     | <span data-ttu-id="af9ab-144">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="af9ab-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="af9ab-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af9ab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9ab-146">**Msiprovidequalifiedcomponent**</span><span class="sxs-lookup"><span data-stu-id="af9ab-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




