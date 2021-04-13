---
title: Antwortdateien
description: Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- Mittlerer l-compilermittell, Antwort Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2019
ms.locfileid: "104388833"
---
# <a name="response-files"></a><span data-ttu-id="6c0c6-104">Antwortdateien</span><span class="sxs-lookup"><span data-stu-id="6c0c6-104">Response Files</span></span>

<span data-ttu-id="6c0c6-105">Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="6c0c6-106">Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="6c0c6-107">Im Gegensatz zu einer Befehlszeile ermöglicht eine Antwortdatei mehrere Zeilen von Optionen und Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="6c0c6-108">Dies kann aufgrund von Einschränkungen der Buildumgebung oder als benutzerfreundlicher Vorgang für Ihren Buildprozess nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="6c0c6-109">Sie können eine mittlerer l-Antwortdatei wie folgt angeben:</span><span class="sxs-lookup"><span data-stu-id="6c0c6-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="6c0c6-110"> **\@ Dateiname** für mittlere</span><span class="sxs-lookup"><span data-stu-id="6c0c6-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="6c0c6-111"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="6c0c6-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="6c0c6-112">Gibt den Namen der Antwortdatei an.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-112">Specifies the name of the response file.</span></span> <span data-ttu-id="6c0c6-113">Der Antwort Dateiname muss unmittelbar auf das @-Zeichen folgen, ohne Leerzeichen zwischen dem @-Zeichen und dem Namen der Antwortdatei.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="6c0c6-114">Die Optionen in einer Antwortdatei werden so interpretiert, als würden Sie an dieser Stelle in der Befehlszeile der Mittell vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="6c0c6-115">Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="6c0c6-116">Sie können den umgekehrten Schrägstrich ( \) zum Verketten von Linien) nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-116">You cannot use the backslash character (\) to concatenate lines.</span></span>

<span data-ttu-id="6c0c6-117">"Mittel l" unterstützt Befehlszeilenargumente, die eine oder mehrere Antwort Dateien enthalten, in Kombination mit anderen Befehls zeilenschaltern:</span><span class="sxs-lookup"><span data-stu-id="6c0c6-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="6c0c6-118">**Mittel l-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**</span><span class="sxs-lookup"><span data-stu-id="6c0c6-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="6c0c6-119">Der mittlerer l-Compiler unterstützt keine netsted Response-Dateien.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-119">The MIDL compiler does not support nested response files.</span></span>

 

 




