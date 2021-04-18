---
description: Die VBScript-Datei WiLstScr.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. In diesem Beispielskript wird der Windows Installer Skript-Viewer veranschaulicht.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Installerskript anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343372"
---
# <a name="view-installer-script"></a><span data-ttu-id="ce4d6-104">Installerskript anzeigen</span><span class="sxs-lookup"><span data-stu-id="ce4d6-104">View Installer Script</span></span>

<span data-ttu-id="ce4d6-105">Die VBScript-Datei WiLstScr.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ce4d6-106">In diesem Beispielskript wird der Windows Installer Skript-Viewer veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="ce4d6-107">Das Beispiel veranschaulicht die Verwendung von:</span><span class="sxs-lookup"><span data-stu-id="ce4d6-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="ce4d6-108">**OpenDatabase-Methode (Installer-Objekt)**</span><span class="sxs-lookup"><span data-stu-id="ce4d6-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="ce4d6-109">[**Lasterrorrecord**](installer-lasterrorrecord.md) -Methode des [**Installer**](installer-object.md) -Objekts</span><span class="sxs-lookup"><span data-stu-id="ce4d6-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="ce4d6-110">[**OpenView**](database-openview.md) -Methode des [**Daten Bank**](database-object.md) Objekts</span><span class="sxs-lookup"><span data-stu-id="ce4d6-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="ce4d6-111">[**Fetch**](view-fetch.md) -Methode des [**View**](view-object.md) -Objekts</span><span class="sxs-lookup"><span data-stu-id="ce4d6-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="ce4d6-112">[**Formattext**](record-formattext.md) -Methode</span><span class="sxs-lookup"><span data-stu-id="ce4d6-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="ce4d6-113">[**FieldCount**](record-fieldcount.md) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce4d6-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="ce4d6-114">[**StringData**](record-stringdata.md) -Eigenschaft des [**Datensatz**](record-object.md) -Objekts</span><span class="sxs-lookup"><span data-stu-id="ce4d6-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="ce4d6-115">\_Transformview-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce4d6-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="ce4d6-116">Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="ce4d6-117">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="ce4d6-118">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="ce4d6-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ce4d6-119">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-119">or if too few arguments are specified.</span></span> <span data-ttu-id="ce4d6-120">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="ce4d6-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ce4d6-121">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ce4d6-122">**cscript-WiLstScr.vbs** *\[ Pfad zum Windows Installer Ausführungs \] Skript*</span><span class="sxs-lookup"><span data-stu-id="ce4d6-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="ce4d6-123">Geben Sie den Pfad zum Ausführungs Skript des Installers an.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="ce4d6-124">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ce4d6-125">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



