---
description: Die VBScript-Datei WiGenXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren. Weitere Informationen finden Sie unter Daten Bank Transformationen.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generieren einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757644"
---
# <a name="generate-a-transform"></a><span data-ttu-id="1a2d2-105">Generieren einer Transformation</span><span class="sxs-lookup"><span data-stu-id="1a2d2-105">Generate a Transform</span></span>

<span data-ttu-id="1a2d2-106">Die VBScript-Datei WiGenXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="1a2d2-107">Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="1a2d2-108">Weitere Informationen finden Sie unter [Daten Bank Transformationen](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="1a2d2-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="1a2d2-109">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="1a2d2-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="1a2d2-110">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="1a2d2-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="1a2d2-111">[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="1a2d2-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="1a2d2-112">[**GenerateTransform-Methode**](database-generatetransform.md) des [ **Datenbankobjekts**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="1a2d2-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="1a2d2-113">Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="1a2d2-114">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="1a2d2-115">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="1a2d2-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="1a2d2-116">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-116">or if too few arguments are specified.</span></span> <span data-ttu-id="1a2d2-117">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="1a2d2-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="1a2d2-118">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="1a2d2-119">**cscript WiGenXfm.vbs \[ Pfad zum ursprünglichen Daten Bank Pfad \] \[ zum überarbeiteten Daten Bank \] \[ Pfad zur Transformations Datei\]**</span><span class="sxs-lookup"><span data-stu-id="1a2d2-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="1a2d2-120">Geben Sie den Pfad zur ursprünglichen Windows Installer Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="1a2d2-121">Geben Sie den Pfad zur überarbeiteten Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-121">Specify the path to the revised database.</span></span> <span data-ttu-id="1a2d2-122">Geben Sie den Pfad zu der zu erstellenden Transformations Datei an.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="1a2d2-123">Wenn der Pfad zur Transformations Datei weggelassen wird, werden die beiden Datenbanken nur verglichen.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="1a2d2-124">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1a2d2-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="1a2d2-125">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1a2d2-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="1a2d2-126">Beachten Sie, dass [ein Lokalisierungs Beispiel](a-localization-example.md) das [Erstellen einer Anpassungs Transformation](generating-a-customization-transform.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1a2d2-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



