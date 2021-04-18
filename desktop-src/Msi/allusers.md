---
Description: Die Eigenschaft ALLUSERS konfiguriert den Installations Kontext des Pakets.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS (Eigenschaft)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354733"
---
# <a name="allusers-property"></a><span data-ttu-id="4ca1a-103">ALLUSERS (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4ca1a-103">ALLUSERS property</span></span>

<span data-ttu-id="4ca1a-104">Die Eigenschaft **ALLUSERS** konfiguriert den Installations Kontext des Pakets.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="4ca1a-105">Der Windows Installer führt eine Installation pro Benutzer oder eine Computer spezifische Installation durch, abhängig von den Zugriffsrechten des Benutzers, davon, ob für die Installation der Anwendung erhöhte Rechte erforderlich sind, den Wert der Eigenschaft " **ALLUSERS** ", den Wert der Eigenschaft " [**msiinstallperuser**](msiinstallperuser.md) " und die Version des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="4ca1a-106">Der Wert der **ALLUSERS** -Eigenschaft bestimmt beim Installations Zeitpunkt den [Installations Kontext](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="4ca1a-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="4ca1a-107">Der Wert 1 der **ALLUSERS** -Eigenschaft gibt den Installations Kontext pro Computer an.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="4ca1a-108">Ein **ALLUSERS** -Eigenschafts Wert einer leeren Zeichenfolge ("") gibt den Installations Kontext pro Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="4ca1a-109">Wenn der Wert der Eigenschaft " **ALLUSERS** " auf 2 festgelegt ist, setzt der Windows Installer den Wert der Eigenschaft " **ALLUSERS** " immer auf "1" zurück und führt eine Installation pro Computer aus, oder der Wert der Eigenschaft " **ALLUSERS** " wird auf eine leere Zeichenfolge ("") zurückgesetzt, und es wird eine benutzerspezifische Installation durchführt.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="4ca1a-110">Der Wert ALLUSERS = 2 ermöglicht dem System, den Wert von **ALLUSERS** und den Installations Kontext zurückzusetzen, abhängig von den Berechtigungen des Benutzers und der Windows-Version.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="4ca1a-111">**Windows 7:** Legen Sie die Eigenschaft " **ALLUSERS** " auf "2" fest, um mithilfe der Eigenschaft " [**msiinstallperuser**](msiinstallperuser.md) " den Installations Kontext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="4ca1a-112">Legen Sie die **msiinstallperuser** -Eigenschaft für eine Computer spezifische Installation auf eine leere Zeichenfolge ("") fest.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="4ca1a-113">Legen Sie für eine Installation pro Benutzer die **msiinstallperuser** -Eigenschaft auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="4ca1a-114">Wenn das Paket nach den in der [Erstellung eines einzelnen Pakets](single-package-authoring.md)beschriebenen Entwicklungs Richtlinien geschrieben wurde, können Benutzer mit Benutzer Zugriff im kontextbezogenen Kontext installieren, ohne UAC-Anmelde Informationen angeben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="4ca1a-115">Wenn der Benutzer über Benutzer Zugriffsberechtigungen verfügt, führt das Installationsprogramm nur dann eine Computer spezifische Installation aus, wenn im UAC-Dialogfeld die Administrator Anmelde Informationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="4ca1a-116">**Windows Vista:** Legen Sie die Eigenschaft **ALLUSERS** auf 2 fest, und Windows Installer entspricht der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC).</span><span class="sxs-lookup"><span data-stu-id="4ca1a-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="4ca1a-117">Wenn der Benutzer über Benutzer Zugriffsberechtigungen und ALLUSERS = 2 verfügt, führt das Installationsprogramm nur dann eine Computer spezifische Installation aus, wenn im UAC-Dialogfeld die Administrator Anmelde Informationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="4ca1a-118">Wenn die Benutzerkontensteuerung aktiviert ist und die richtigen Administrator Anmelde Informationen nicht bereitgestellt werden, tritt bei der Installation ein Fehler auf, der besagt, dass Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="4ca1a-119">Wenn die UAC durch den Registrierungsschlüssel, die Gruppenrichtlinie oder die Systemsteuerung deaktiviert ist, wird das Dialogfeld UAC nicht angezeigt, und bei der Installation tritt ein Fehler mit dem Hinweis auf, dass Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="4ca1a-120">**Windows XP:** Legen Sie die Eigenschaft " **ALLUSERS** " auf 2 fest, und Windows Installer führt eine Installation pro Benutzer aus, wenn der Benutzer über Benutzer Zugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="4ca1a-121">Wenn der Wert der **ALLUSERS** -Eigenschaft nicht gleich 2 ist, ignoriert der Windows Installer den Wert der [**msiinstallperuser**](msiinstallperuser.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="4ca1a-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ca1a-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="4ca1a-123">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="4ca1a-124">Standardwert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-124">Default Value</span></span>

<span data-ttu-id="4ca1a-125">Der empfohlene Standard Installations Kontext ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="4ca1a-126">Wenn **ALLUSERS** nicht festgelegt ist, führt das Installationsprogramm eine Installation pro Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="4ca1a-127">Sie können sicherstellen, dass die Eigenschaft " **ALLUSERS** " nicht festgelegt wurde, indem Sie Ihren Wert auf eine leere Zeichenfolge (""), ALLUSERS = "" festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca1a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ca1a-128">Remarks</span></span>

<span data-ttu-id="4ca1a-129">Der [Installations Kontext](installation-context.md) bestimmt die Werte der Eigenschaften [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**templatefolder**](templatefolder.md), [**admintoolsfolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)und [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca1a-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="4ca1a-130">Der Installations Kontext bestimmt die Teile der Registrierung, in denen Einträge in der [Registrierungs Tabelle](registry-table.md) und der [removeregistry-Tabelle](removeregistry-table.md)mit-1 in der Stamm Spalte geschrieben oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca1a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca1a-131">Requirements</span></span>



| <span data-ttu-id="4ca1a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ca1a-132">Requirement</span></span> | <span data-ttu-id="4ca1a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca1a-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca1a-134">Version</span><span class="sxs-lookup"><span data-stu-id="4ca1a-134">Version</span></span><br/> | <span data-ttu-id="4ca1a-135">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4ca1a-136">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4ca1a-137">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4ca1a-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4ca1a-138">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca1a-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ca1a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ca1a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca1a-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ca1a-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4ca1a-141">**Msiinstallperuser**</span><span class="sxs-lookup"><span data-stu-id="4ca1a-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="4ca1a-142">Installations Kontext</span><span class="sxs-lookup"><span data-stu-id="4ca1a-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="4ca1a-143">Erstellung eines einzelnen Pakets</span><span class="sxs-lookup"><span data-stu-id="4ca1a-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




