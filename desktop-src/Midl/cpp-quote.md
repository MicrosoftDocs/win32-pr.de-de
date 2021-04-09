---
title: cpp_quote-Attribut
description: Das cpp- \_ Anführungszeichen Schlüsselwort weist die Mittel l an, die angegebene Zeichenfolge ohne Anführungszeichen in die generierte Header Datei auszugeben.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote Attribut-Mittel l
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038110"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="841d8-104">cpp- \_ Anführungszeichen Attribut</span><span class="sxs-lookup"><span data-stu-id="841d8-104">cpp\_quote attribute</span></span>

<span data-ttu-id="841d8-105">Das **cpp- \_ Anführungs** Zeichen Schlüsselwort weist die Mittel l an, die angegebene Zeichenfolge ohne Anführungszeichen in die generierte Header Datei auszugeben.</span><span class="sxs-lookup"><span data-stu-id="841d8-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="841d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="841d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841d8-107">*string*</span><span class="sxs-lookup"><span data-stu-id="841d8-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="841d8-108">Gibt eine Zeichenfolge in Anführungszeichen an, die in der generierten Header Datei ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="841d8-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="841d8-109">Die Zeichenfolge muss in Anführungszeichen eingeschlossen werden, um zu verhindern, dass der C-Präprozessor</span><span class="sxs-lookup"><span data-stu-id="841d8-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="841d8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="841d8-110">Remarks</span></span>

<span data-ttu-id="841d8-111">In der IDL-Datei angezeigte Vorverarbeitung-Direktiven der c-Sprache werden vom Präprozessor des C-Compilers verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="841d8-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="841d8-112">Die **\# define** -Direktiven in der IDL-Datei sind während der Mitte der Kompilierung verfügbar, sind aber für den C-Compiler nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="841d8-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="841d8-113">Wenn der Präprozessor z. b. auf die Direktive " \# Windows 4 definieren" stößt, ersetzt der Präprozessor alle Vorkommen von "Windows" in der IDL-Datei durch "4".</span><span class="sxs-lookup"><span data-stu-id="841d8-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="841d8-114">Das Symbol "Windows" ist während der Kompilierung der C-Sprache nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="841d8-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="841d8-115">Um zuzulassen, dass die c-präprozessormakrodefinitionen den Mittel l-Compiler an den c-Compiler übergeben, verwenden Sie die- **\# pragma \_** -Anweisung "-Echo" oder " **cpp- \_ Anführungs** Zeichen".</span><span class="sxs-lookup"><span data-stu-id="841d8-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="841d8-116">Diese Direktiven weisen den Mittelwert Compiler an, eine Header Datei zu generieren, die die Parameter Zeichenfolge enthält, wobei die Anführungszeichen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="841d8-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="841d8-117">Die Anweisungs-und **cpp- \_** Anweisungs Direktiven von **\# pragma \_** sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="841d8-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="841d8-118">Der mittlerer l-Compiler fügt die in den **cpp- \_ Anführungs** Zeichen und- [**pragma**](pragma.md) -Direktiven angegebenen Zeichen folgen in die Header Datei in der Reihenfolge, in der Sie in der IDL-Datei angegeben sind, und relativ zu anderen Schnittstellen Komponenten in der IDL-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="841d8-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="841d8-119">Die Zeichen folgen sollten in der Regel im Textabschnitt der IDL-Datei Schnittstelle nach allen [**Import**](import.md) Vorgängen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="841d8-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="841d8-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="841d8-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="841d8-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="841d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841d8-122">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="841d8-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="841d8-123">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="841d8-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="841d8-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="841d8-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




