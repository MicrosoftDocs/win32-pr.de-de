---
title: MOF-Zeichen folgen
description: Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die in der Regel als lesbarer Text gedacht ist.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863795"
---
# <a name="mof-strings"></a><span data-ttu-id="6d57e-103">MOF-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="6d57e-103">MOF strings</span></span>

<span data-ttu-id="6d57e-104">Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die in der Regel als lesbarer Text gedacht ist.</span><span class="sxs-lookup"><span data-stu-id="6d57e-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="6d57e-105">MOF beschreibt zwei Arten von Zeichen folgen, die verwenden, um einzelne oder mehrere Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6d57e-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="6d57e-106">MOF verfügt auch über eine Reihe von Regeln, die die Verwendung von Anführungszeichen innerhalb einer Zeichenfolge beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6d57e-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="6d57e-107">In der folgenden Tabelle sind die Zeichen folgen Datentypen für MOF aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d57e-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="6d57e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6d57e-108">Data type</span></span>  | <span data-ttu-id="6d57e-109">Automatisierungstyp</span><span class="sxs-lookup"><span data-stu-id="6d57e-109">Automation type</span></span> | <span data-ttu-id="6d57e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d57e-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d57e-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="6d57e-111">**char16**</span></span> | <span data-ttu-id="6d57e-112">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="6d57e-112">**VT\_I2**</span></span>      | <span data-ttu-id="6d57e-113">Einzelnes 16-Bit-Unicode-Zeichen im UCS-2-Format (Universal Character Set 2)</span><span class="sxs-lookup"><span data-stu-id="6d57e-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="6d57e-114">**string**</span><span class="sxs-lookup"><span data-stu-id="6d57e-114">**string**</span></span> | <span data-ttu-id="6d57e-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="6d57e-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="6d57e-116">Unicode-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6d57e-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="6d57e-117">Beachten Sie beim Schreiben von Zeichen folgen für MOF die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="6d57e-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="6d57e-118">Umschließen Sie Einzelzeichen Konstanten in einfache Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="6d57e-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="6d57e-119">Wenn Sie keine einfachen Anführungszeichen mit Einzelzeichen Konstanten verwenden, müssen Sie die ganzzahlige Darstellung des Unicode-Zeichen Werts verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d57e-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="6d57e-120">Optional können Sie das Zeichen mit der \\ x-Escapesequenz aus dem American National Standards Institute (ANSI) C-Standard angeben, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="6d57e-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="6d57e-121">Da MOF auf Unicode basiert, können Sie auch 16-Bit-Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="6d57e-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="6d57e-122">Beachten Sie, dass Einzelzeichen Konstanten im ANSI C-Format in doppelte Anführungszeichen eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="6d57e-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="6d57e-123">Umschließen Sie Zeichen folgen in doppelte Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="6d57e-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="6d57e-124">Verketten Sie nachfolgende Anführungszeichen folgen mit einem oder mehreren Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6d57e-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="6d57e-125">Verwenden Sie eine Escapesequenz mit einem umgekehrten Schrägstrich, um Anführungszeichen in eine Zeichenfolge einzubetten.</span><span class="sxs-lookup"><span data-stu-id="6d57e-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="6d57e-126">Im folgenden Beispiel wird beschrieben, wie Zeichen folgen Eigenschaften und ein Zeichen folgen Parameter initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="6d57e-126">The following example describes how to initialize string properties and a string parameter:</span></span>

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




