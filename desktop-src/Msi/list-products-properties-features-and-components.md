---
description: Die VBScript-Datei WiLstPrd.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Das Beispielskript stellt eine Verbindung mit einem Installerobjekt her und listet registrierte Produkte und Produktinformationen auf.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Auflisten von Produkten, Eigenschaften, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347189"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="89213-104">Auflisten von Produkten, Eigenschaften, Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="89213-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="89213-105">Die VBScript-Datei WiLstPrd.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="89213-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="89213-106">Das Beispielskript stellt eine Verbindung mit einem [**Installerobjekt**](installer-object.md) her und listet registrierte Produkte und Produktinformationen auf.</span><span class="sxs-lookup"><span data-stu-id="89213-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="89213-107">In diesem Beispiel wird die Verwendung von veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="89213-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="89213-108">**ProductInfo-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="89213-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="89213-109">**Productstate-Eigenschaft (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="89213-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="89213-110">**Products-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="89213-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="89213-111">**Features-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="89213-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="89213-112">**Featureparent (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="89213-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="89213-113">**Featurestate (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="89213-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="89213-114">**Komponenten Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="89213-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="89213-115">**Componentclients (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="89213-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="89213-116">**Componentpath (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="89213-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="89213-117">**Lasterrorrecord-Methode**</span><span class="sxs-lookup"><span data-stu-id="89213-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="89213-118">[**REGISTRYVALUE-Methode**](installer-registryvalue.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="89213-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="89213-119">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89213-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="89213-120">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="89213-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="89213-121">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="89213-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="89213-122">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89213-122">or if too few arguments are specified.</span></span> <span data-ttu-id="89213-123">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ Pfad zur Datei \] .</span><span class="sxs-lookup"><span data-stu-id="89213-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="89213-124">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="89213-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="89213-125">**cscript-WiLstPrd.vbs Optionen für den \[ Produktnamen \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="89213-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="89213-126">Geben Sie den Produktnamen für die Groß-/Kleinschreibung oder die Produkt-ID-GUID des installierten oder angekündigten Produkts an.</span><span class="sxs-lookup"><span data-stu-id="89213-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="89213-127">Wenn kein Produkt oder keine Optionen angegeben werden, listet das Installationsprogramm alle Produkte auf, die auf dem System installiert oder angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="89213-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="89213-128">Beachten Sie, dass es sich bei diesen Optionen nicht um Switches handelt, sodass Sie keinen Schrägstrich (/) in der Befehlszeile voranstellen sollten.</span><span class="sxs-lookup"><span data-stu-id="89213-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="89213-129">Die folgenden Optionen können durch Verkettung der Buchstaben kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="89213-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="89213-130">Beispiel: "PC" zum Auflisten der Eigenschaften und der installierten Komponenten der Produkte.</span><span class="sxs-lookup"><span data-stu-id="89213-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="89213-131">Option</span><span class="sxs-lookup"><span data-stu-id="89213-131">Option</span></span>               | <span data-ttu-id="89213-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89213-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89213-133">keine Optionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="89213-133">no options specified</span></span> | <span data-ttu-id="89213-134">Listet die Eigenschaften der Produkte auf.</span><span class="sxs-lookup"><span data-stu-id="89213-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="89213-135">p</span><span class="sxs-lookup"><span data-stu-id="89213-135">p</span></span>                    | <span data-ttu-id="89213-136">Listet die Eigenschaften der Produkte auf.</span><span class="sxs-lookup"><span data-stu-id="89213-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="89213-137">f</span><span class="sxs-lookup"><span data-stu-id="89213-137">f</span></span>                    | <span data-ttu-id="89213-138">Auflisten der Features der Produkte, der übergeordneten Funktionen und der Installations Zustände</span><span class="sxs-lookup"><span data-stu-id="89213-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="89213-139">c</span><span class="sxs-lookup"><span data-stu-id="89213-139">c</span></span>                    | <span data-ttu-id="89213-140">Listet die installierten Komponenten der Produkte auf.</span><span class="sxs-lookup"><span data-stu-id="89213-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="89213-141">d</span><span class="sxs-lookup"><span data-stu-id="89213-141">d</span></span>                    | <span data-ttu-id="89213-142">Listen Sie den Wert unter " **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDLLs** " für die Schlüsseldateien der Komponente "Products" auf.</span><span class="sxs-lookup"><span data-stu-id="89213-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="89213-143">Weitere Informationen finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) für weitere Skript Beispiele.</span><span class="sxs-lookup"><span data-stu-id="89213-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="89213-144">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="89213-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



