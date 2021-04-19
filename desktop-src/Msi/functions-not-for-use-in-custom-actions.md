---
description: Die folgenden Datenbankfunktionen müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funktionen, die nicht für benutzerdefinierte Aktionen verwendet werden können
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349504"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="f134a-103">Funktionen, die nicht für benutzerdefinierte Aktionen verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="f134a-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="f134a-104">Die folgenden [Datenbankfunktionen](database-functions.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f134a-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="f134a-105">**Msikonfigurireproduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="f134a-106">**Msikonfigurireproduktions-ctex**</span><span class="sxs-lookup"><span data-stu-id="f134a-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="f134a-107">**Msikreatetransformsummaryinfo**</span><span class="sxs-lookup"><span data-stu-id="f134a-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="f134a-108">**Msidatabaseapplytransform**</span><span class="sxs-lookup"><span data-stu-id="f134a-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="f134a-109">**Msidatabasecommit**</span><span class="sxs-lookup"><span data-stu-id="f134a-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="f134a-110">**Msidatabaseexport**</span><span class="sxs-lookup"><span data-stu-id="f134a-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="f134a-111">**Msidatabasegeneratetransform**</span><span class="sxs-lookup"><span data-stu-id="f134a-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="f134a-112">**Msidatabaseimport**</span><span class="sxs-lookup"><span data-stu-id="f134a-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="f134a-113">**Msidatabasemerge**</span><span class="sxs-lookup"><span data-stu-id="f134a-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="f134a-114">**Msienablelog**</span><span class="sxs-lookup"><span data-stu-id="f134a-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="f134a-115">**Msienableuipreview**</span><span class="sxs-lookup"><span data-stu-id="f134a-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="f134a-116">**Msigetdatabasestate**</span><span class="sxs-lookup"><span data-stu-id="f134a-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="f134a-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="f134a-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="f134a-118">**Msipreviewbillboard**</span><span class="sxs-lookup"><span data-stu-id="f134a-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="f134a-119">**Msipreviewdialog**</span><span class="sxs-lookup"><span data-stu-id="f134a-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="f134a-120">**Msireinstallproduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="f134a-121">**Msiseeltexternalui**</span><span class="sxs-lookup"><span data-stu-id="f134a-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="f134a-122">**Msiseeltexternaluirecord**</span><span class="sxs-lookup"><span data-stu-id="f134a-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="f134a-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="f134a-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="f134a-124">Die folgenden [Installer-Funktionen](installer-function-reference.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f134a-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="f134a-125">**Msiapplypatch**</span><span class="sxs-lookup"><span data-stu-id="f134a-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="f134a-126">**Msicollectuserinfo**</span><span class="sxs-lookup"><span data-stu-id="f134a-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="f134a-127">**Msikonfigurierfeature**</span><span class="sxs-lookup"><span data-stu-id="f134a-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="f134a-128">**Msikonfigurireproduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="f134a-129">**Msikonfigurireproduktions-ctex**</span><span class="sxs-lookup"><span data-stu-id="f134a-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="f134a-130">**Msienablelog**</span><span class="sxs-lookup"><span data-stu-id="f134a-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="f134a-131">**Msigetfeatureinfo**</span><span class="sxs-lookup"><span data-stu-id="f134a-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="f134a-132">**Msigetproductcode**</span><span class="sxs-lookup"><span data-stu-id="f134a-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="f134a-133">**Msigetproductproperty**</span><span class="sxs-lookup"><span data-stu-id="f134a-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="f134a-134">**Msiinstallmissingcomponent**</span><span class="sxs-lookup"><span data-stu-id="f134a-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="f134a-135">**Msiinstallmissingfile**</span><span class="sxs-lookup"><span data-stu-id="f134a-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="f134a-136">**Msiinstallproduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="f134a-137">**Msiopenpackage**</span><span class="sxs-lookup"><span data-stu-id="f134a-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="f134a-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="f134a-139">**Msireinstallfeature**</span><span class="sxs-lookup"><span data-stu-id="f134a-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="f134a-140">**Msireinstallproduct**</span><span class="sxs-lookup"><span data-stu-id="f134a-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="f134a-141">**Msiseeltexternalui**</span><span class="sxs-lookup"><span data-stu-id="f134a-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="f134a-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="f134a-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="f134a-143">**Msiusefeature**</span><span class="sxs-lookup"><span data-stu-id="f134a-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="f134a-144">**Msiusefeatureex**</span><span class="sxs-lookup"><span data-stu-id="f134a-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="f134a-145">**Msiverifypackage**</span><span class="sxs-lookup"><span data-stu-id="f134a-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="f134a-146">Die folgenden [Installer-Funktionen](installer-function-reference.md) müssen nie von einer benutzerdefinierten Aktion aufgerufen werden, wenn eine andere Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f134a-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="f134a-147">Sie können von einer benutzerdefinierten Aktion aufgerufen werden, die keine andere Installation startet.</span><span class="sxs-lookup"><span data-stu-id="f134a-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="f134a-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="f134a-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="f134a-149">**Msiprovidequalifiedcomponent**</span><span class="sxs-lookup"><span data-stu-id="f134a-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="f134a-150">**Msiprovide qualifiedcomponumtex**</span><span class="sxs-lookup"><span data-stu-id="f134a-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="f134a-151">Eine benutzerdefinierte Aktion sollte nie einen neuen Thread erzeugen, der Windows Installer Funktionen verwendet, um den Funktionsstatus, den Komponenten Status oder das Senden von Nachrichten von einem Steuerungs Ereignis zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f134a-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="f134a-152">Wenn Sie versuchen, dies zu tun, schlägt die Installation fehl.</span><span class="sxs-lookup"><span data-stu-id="f134a-152">Attempting to do this causes the installation to fail.</span></span>

 

 



