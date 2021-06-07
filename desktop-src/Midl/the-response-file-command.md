---
title: Befehl "Antwortdatei"
description: Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Befehlszeilenreferenz MIDL, Befehl "Antwortdatei"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387666"
---
# <a name="the-response-file-command"></a><span data-ttu-id="e1c74-104">Befehl "Antwortdatei"</span><span class="sxs-lookup"><span data-stu-id="e1c74-104">The Response File Command</span></span>

<span data-ttu-id="e1c74-105">Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält.</span><span class="sxs-lookup"><span data-stu-id="e1c74-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="e1c74-106">Im Gegensatz zu einer Befehlszeile lässt eine Antwortdatei mehrere Zeilen mit Optionen und Dateinamen zu.</span><span class="sxs-lookup"><span data-stu-id="e1c74-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="e1c74-107">Dies kann aufgrund von Einschränkungen Ihrer Buildumgebung oder zur Vereinfachung Ihres Buildprozesses nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="e1c74-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="e1c74-108">Switch-Optionen</span><span class="sxs-lookup"><span data-stu-id="e1c74-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="e1c74-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*\_Antwortdatei*</span><span class="sxs-lookup"><span data-stu-id="e1c74-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="e1c74-110">Gibt den Namen einer Antwortdatei an.</span><span class="sxs-lookup"><span data-stu-id="e1c74-110">Specifies the name of a response file.</span></span> <span data-ttu-id="e1c74-111">Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e1c74-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="e1c74-112">Zwischen dem @-Zeichen und dem Namen der Antwortdatei ist kein Leerzeichen zulässig.</span><span class="sxs-lookup"><span data-stu-id="e1c74-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1c74-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1c74-113">Remarks</span></span>

<span data-ttu-id="e1c74-114">Als Alternative zum Platzieren aller Optionen, die einem Schalter in der Befehlszeile zugeordnet sind, akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1c74-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="e1c74-115">Optionen in einer Antwortdatei werden so interpretiert, als ob sie an diesem Speicherort in der MIDL-Befehlszeile vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e1c74-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="e1c74-116">Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="e1c74-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="e1c74-117">Der schräge Schrägstrich ( ) kann nicht verwendet werden, um Zeilen \\ zu verketten.</span><span class="sxs-lookup"><span data-stu-id="e1c74-117">The backslash character (\\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="e1c74-118">Wenn er Teil einer Zeichenfolge in Anführungszeichen in der Antwortdatei ist, kann der schräge Schrägstrich nur vor einem anderen schrägen Schrägstrich oder vor einem doppelten Anführungszeichen () verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1c74-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="e1c74-119">Wenn er nicht Teil einer Zeichenfolge in Anführungszeichen ist, kann der schräge Schrägstrich nur vor einem doppelten Anführungszeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1c74-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="e1c74-120">MIDL unterstützt Befehlszeilenargumente, die eine oder mehrere Antwortdateien in Kombination mit anderen Befehlszeilenschaltern enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1c74-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="e1c74-121">Der MIDL-Compiler unterstützt keine geschachtelten Antwortdateien.</span><span class="sxs-lookup"><span data-stu-id="e1c74-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="e1c74-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1c74-122">Examples</span></span>

<span data-ttu-id="e1c74-123">**Midl @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="e1c74-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="e1c74-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="e1c74-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c74-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1c74-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c74-126">Allgemeine MIDL-Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="e1c74-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




