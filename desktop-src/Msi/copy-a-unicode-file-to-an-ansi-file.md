---
description: Die VBScript-Datei WiToAnsi.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie ein Skript zum Umschreiben einer Unicode-Textdatei als ANSI-Textdatei verwendet wird.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Kopieren einer Unicode-Datei in eine ANSI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866092"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="848e5-104">Kopieren einer Unicode-Datei in eine ANSI-Datei</span><span class="sxs-lookup"><span data-stu-id="848e5-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="848e5-105">Die VBScript-Datei WiToAnsi.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="848e5-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="848e5-106">Dieses Beispiel zeigt, wie ein Skript zum Umschreiben einer Unicode-Textdatei als ANSI-Textdatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="848e5-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="848e5-107">Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich.</span><span class="sxs-lookup"><span data-stu-id="848e5-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="848e5-108">Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="848e5-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="848e5-109">Hilfe wird angezeigt, wenn das erste Argument/?</span><span class="sxs-lookup"><span data-stu-id="848e5-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="848e5-110">oder, wenn zu wenige Argumente angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="848e5-110">or if too few arguments are specified.</span></span> <span data-ttu-id="848e5-111">Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .</span><span class="sxs-lookup"><span data-stu-id="848e5-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="848e5-112">Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="848e5-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="848e5-113">**cscript-WiToAnsi.vbs \[ Pfad zum Unicode- \] \[ Dateipfad zur ANSI-Datei\]**</span><span class="sxs-lookup"><span data-stu-id="848e5-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="848e5-114">Geben Sie die Unicode-Textdatei an, die konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="848e5-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="848e5-115">Geben Sie die ANSI-Textdatei an, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="848e5-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="848e5-116">Wenn keine ANSI-Datei angegeben ist, wird die Unicode-Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="848e5-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="848e5-117">Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="848e5-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="848e5-118">Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="848e5-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



