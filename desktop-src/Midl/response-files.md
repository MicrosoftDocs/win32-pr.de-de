---
title: Antwortdateien
description: Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL-Compiler MIDL, Antwortdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387070"
---
# <a name="response-files"></a><span data-ttu-id="9c08e-104">Antwortdateien</span><span class="sxs-lookup"><span data-stu-id="9c08e-104">Response Files</span></span>

<span data-ttu-id="9c08e-105">Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c08e-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="9c08e-106">Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält.</span><span class="sxs-lookup"><span data-stu-id="9c08e-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="9c08e-107">Im Gegensatz zu einer Befehlszeile lässt eine Antwortdatei mehrere Zeilen mit Optionen und Dateinamen zu.</span><span class="sxs-lookup"><span data-stu-id="9c08e-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="9c08e-108">Dies kann aufgrund von Einschränkungen Ihrer Buildumgebung oder zur Vereinfachung des Buildprozesses nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="9c08e-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="9c08e-109">Sie können eine MIDL-Antwortdatei wie die folgende angeben:</span><span class="sxs-lookup"><span data-stu-id="9c08e-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="9c08e-110">**midl** **\@ filename**</span><span class="sxs-lookup"><span data-stu-id="9c08e-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="9c08e-111"><span id="filename"></span><span id="FILENAME"></span>*Dateiname*</span><span class="sxs-lookup"><span data-stu-id="9c08e-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9c08e-112">Gibt den Namen der Antwortdatei an.</span><span class="sxs-lookup"><span data-stu-id="9c08e-112">Specifies the name of the response file.</span></span> <span data-ttu-id="9c08e-113">Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen, ohne Leerzeichen zwischen dem @-Zeichen und dem Namen der Antwortdatei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c08e-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="9c08e-114">Optionen in einer Antwortdatei werden so interpretiert, als wären sie an dieser Stelle in der MIDL-Befehlszeile vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9c08e-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="9c08e-115">Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="9c08e-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="9c08e-116">Sie können den umgekehrten Schrägstrich () nicht \\ verwenden, um Zeilen zu verketten.</span><span class="sxs-lookup"><span data-stu-id="9c08e-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="9c08e-117">MIDL unterstützt Befehlszeilenargumente, die eine oder mehrere Antwortdateien enthalten, kombiniert mit anderen Befehlszeilenschaltern:</span><span class="sxs-lookup"><span data-stu-id="9c08e-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="9c08e-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="9c08e-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="9c08e-119">Der MIDL-Compiler unterstützt keine geschachtelten Antwortdateien.</span><span class="sxs-lookup"><span data-stu-id="9c08e-119">The MIDL compiler does not support nested response files.</span></span>

 

 




