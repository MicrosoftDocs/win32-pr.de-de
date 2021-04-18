---
description: Die Eigenschaften msiinstallperuser und ALLUSERS können vom Benutzer zur Installationszeit, über die Benutzeroberfläche oder über die Befehlszeile festgelegt werden, um anzufordern, dass die Windows Installer ein Paket mit zwei Zweck für den aktuellen Benutzer oder alle Benutzer des Computers installieren.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Msiinstallperuser (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357559"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="c2d21-103">Msiinstallperuser (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2d21-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="c2d21-104">Die Eigenschaften **msiinstallperuser** und [**ALLUSERS**](allusers.md) können vom Benutzer zur Installationszeit, über die Benutzeroberfläche oder über die Befehlszeile festgelegt werden, um anzufordern, dass die Windows Installer ein Paket mit zwei Zweck für den aktuellen Benutzer oder alle Benutzer des Computers installieren.</span><span class="sxs-lookup"><span data-stu-id="c2d21-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="c2d21-105">Um die **msiinstallperuser** -Eigenschaft verwenden zu können, muss der Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " 2 sein, und das Paket muss erstellt worden sein, damit die Installation entweder im Benutzer-oder in einem computerbezogenen Kontext erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="c2d21-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="c2d21-106">Informationen zum Erstellen eines Pakets mit zwei Zweck, finden Sie unter [Erstellen einzelner Pakete](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="c2d21-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="c2d21-107">Wenn der Wert der Eigenschaft " **ALLUSERS** " nicht gleich 2 ist, wird der Wert der Eigenschaft " **msiinstallperuser** " ignoriert und hat keine Auswirkung auf die Installation.</span><span class="sxs-lookup"><span data-stu-id="c2d21-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="c2d21-108">Der Wert der **msiinstallperuser** -Eigenschaft wird bei der Installation des Pakets mit Windows Installer 4,5 oder früher ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c2d21-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="c2d21-109">Der Benutzer kann den Wert der Eigenschaft " **msiinstallperuser** " auf eine leere Zeichenfolge ("") und den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" [festlegen, indem](installation-context.md)er eine erstellte Benutzeroberfläche oder eine Befehlszeile verwendet. Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c2d21-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="c2d21-110">Der Benutzer kann den Wert der Eigenschaft " **msiinstallperuser** " auf 1 und den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" festlegen, indem er eine erstellte Benutzeroberfläche oder eine Befehlszeile verwendet, um anzufordern, dass der Windows Installer das Paket mit zwei Zweck im [Installations Kontext](installation-context.md)pro Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="c2d21-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="c2d21-111">Wenn der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft nicht gleich 2 ist, ignoriert der Windows Installer den Wert der **msiinstallperuser** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c2d21-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="c2d21-112">Wenn Windows Installer die Anwendung im computerspezifischen Kontext installiert, wird der Wert der Eigenschaft " **ALLUSERS** " auf 1 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c2d21-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="c2d21-113">Wenn Windows Installer die Anwendung im kontextbezogenen Kontext installiert, setzt Sie den Wert der **ALLUSERS** -Eigenschaft auf eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="c2d21-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="c2d21-114">Anwendungen, die pro Benutzer installiert wurden, erhalten daher alle Updates oder Reparaturen pro Benutzer, und pro Computer installierte Anwendungen erhalten Updates oder Reparaturen auf Computer Basis.</span><span class="sxs-lookup"><span data-stu-id="c2d21-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="c2d21-115">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** die **msiinstallperuser** -Eigenschaft wird von früheren Versionen als Windows Installer 5,0 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c2d21-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="c2d21-116">Standardwert</span><span class="sxs-lookup"><span data-stu-id="c2d21-116">Default Value</span></span>

<span data-ttu-id="c2d21-117">Der empfohlene Standard Installations Kontext ist pro Benutzer für ein Paket mit zwei Zweck.</span><span class="sxs-lookup"><span data-stu-id="c2d21-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="c2d21-118">Erstellen Sie msiinstallperuser = 1 und ALLUSERS = 2 in der [Eigenschaften Tabelle](property-table.md) des Pakets mit zwei Zweck, um pro Benutzer als Standard Installations Kontext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c2d21-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d21-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2d21-119">Remarks</span></span>

<span data-ttu-id="c2d21-120">Sie können sicherstellen, dass die **msiinstallperuser** -Eigenschaft nicht festgelegt wurde, indem Sie Ihren Wert auf eine leere Zeichenfolge (""), msiinstallperuser = "" festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2d21-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="c2d21-121">Der Installations Kontext bestimmt die Werte der Eigenschaften [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**templatefolder**](templatefolder.md), [**admintoolsfolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)und [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d21-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="c2d21-122">Der Installations Kontext bestimmt die Teile der Registrierung, in denen Einträge in der [Registrierungs Tabelle](registry-table.md) und der [removeregistry-Tabelle](removeregistry-table.md)mit-1 in der Stamm Spalte geschrieben oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c2d21-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="c2d21-123">Weitere Informationen zum Installations Kontext finden Sie unter [Installations Kontext](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="c2d21-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d21-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2d21-124">Requirements</span></span>



| <span data-ttu-id="c2d21-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2d21-125">Requirement</span></span> | <span data-ttu-id="c2d21-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c2d21-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d21-127">Version</span><span class="sxs-lookup"><span data-stu-id="c2d21-127">Version</span></span><br/> | <span data-ttu-id="c2d21-128">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c2d21-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c2d21-129">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d21-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2d21-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2d21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d21-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2d21-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c2d21-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="c2d21-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="c2d21-133">Installations Kontext</span><span class="sxs-lookup"><span data-stu-id="c2d21-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="c2d21-134">Erstellung eines einzelnen Pakets</span><span class="sxs-lookup"><span data-stu-id="c2d21-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




