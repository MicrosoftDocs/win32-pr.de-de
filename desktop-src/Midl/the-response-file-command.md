---
title: Der Antwortdatei Befehl.
description: Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Befehlszeilen Referenz-Mittell, Antwortdatei Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947964"
---
# <a name="the-response-file-command"></a><span data-ttu-id="dc176-104">Der Antwortdatei Befehl.</span><span class="sxs-lookup"><span data-stu-id="dc176-104">The Response File Command</span></span>

<span data-ttu-id="dc176-105">Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält.</span><span class="sxs-lookup"><span data-stu-id="dc176-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="dc176-106">Im Gegensatz zu einer Befehlszeile ermöglicht eine Antwortdatei mehrere Zeilen von Optionen und Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="dc176-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="dc176-107">Dies kann aufgrund von Einschränkungen ihrer Buildumgebung oder für Ihren Buildprozess nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="dc176-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="dc176-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="dc176-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="dc176-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*Antwort \_ Datei*</span><span class="sxs-lookup"><span data-stu-id="dc176-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="dc176-110">Gibt den Namen einer Antwortdatei an.</span><span class="sxs-lookup"><span data-stu-id="dc176-110">Specifies the name of a response file.</span></span> <span data-ttu-id="dc176-111">Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="dc176-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="dc176-112">Zwischen dem @-Zeichen und dem Namen der Antwortdatei ist kein Leerraum zulässig.</span><span class="sxs-lookup"><span data-stu-id="dc176-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc176-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc176-113">Remarks</span></span>

<span data-ttu-id="dc176-114">Als Alternative zum Platzieren aller Optionen, die einem Switch in der Befehlszeile zugeordnet sind, akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc176-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="dc176-115">Optionen in einer Antwortdatei werden so interpretiert, als ob Sie an dieser Stelle in der Mittell-Befehlszeile vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dc176-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="dc176-116">Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="dc176-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="dc176-117">Der umgekehrte Schrägstrich ( \) kann nicht zum Verketten von Zeilen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc176-117">The backslash character (\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="dc176-118">Wenn es Teil einer Zeichenfolge in Anführungszeichen in der Antwortdatei ist, kann der umgekehrte Schrägstrich nur vor einem anderen umgekehrten Schrägstrich oder vor einem doppelten Anführungszeichen (") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc176-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="dc176-119">Wenn Sie nicht Teil einer Zeichenfolge in Anführungszeichen ist, kann der umgekehrte Schrägstrich nur vor einem doppelten Anführungszeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc176-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="dc176-120">"Mittel l" unterstützt Befehlszeilenargumente, die eine oder mehrere Antwort Dateien in Kombination mit anderen Befehls zeilenschaltern enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc176-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="dc176-121">Der mittlerer l-Compiler unterstützt keine netsted Response-Dateien.</span><span class="sxs-lookup"><span data-stu-id="dc176-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="dc176-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc176-122">Examples</span></span>

<span data-ttu-id="dc176-123">**MIDL @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="dc176-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="dc176-124">**Mittel l-Oicf @midl1.rsp -"Win32 @midl2.rsp . idl" für Win32**</span><span class="sxs-lookup"><span data-stu-id="dc176-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc176-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc176-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc176-126">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="dc176-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




