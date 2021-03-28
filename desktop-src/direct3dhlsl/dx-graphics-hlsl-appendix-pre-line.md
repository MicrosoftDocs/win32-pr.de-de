---
title: " line-Direktive"
description: Eine Präprozessordirektive, die die intern gespeicherte Zeilennummer und den Dateinamen des Compilers auf die angegebenen Werte festlegt.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- line-Direktive HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389151"
---
# <a name="line-directive"></a><span data-ttu-id="8a333-104">\#line-Direktive</span><span class="sxs-lookup"><span data-stu-id="8a333-104">\#line Directive</span></span>

<span data-ttu-id="8a333-105">Eine Präprozessordirektive, die die intern gespeicherte Zeilennummer und den Dateinamen des Compilers auf die angegebenen Werte festlegt.</span><span class="sxs-lookup"><span data-stu-id="8a333-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="8a333-106">\#Zeile *LineNumber* "*Dateiname*"</span><span class="sxs-lookup"><span data-stu-id="8a333-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8a333-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a333-107">Parameters</span></span>



| <span data-ttu-id="8a333-108">Element</span><span class="sxs-lookup"><span data-stu-id="8a333-108">Item</span></span>                                                                                                                              | <span data-ttu-id="8a333-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a333-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a333-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*LineNumber*</span><span class="sxs-lookup"><span data-stu-id="8a333-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="8a333-111">Die festzulegende Zeilennummer.</span><span class="sxs-lookup"><span data-stu-id="8a333-111">Line number to set.</span></span> <span data-ttu-id="8a333-112">Dies kann eine beliebige ganzzahlige Konstante sein.</span><span class="sxs-lookup"><span data-stu-id="8a333-112">This can be any integer constant.</span></span> <span data-ttu-id="8a333-113">Die Makro Ersetzung kann für die Vorverarbeitungs Token ausgeführt werden, solange das Ergebnis die richtige Syntax ergibt.</span><span class="sxs-lookup"><span data-stu-id="8a333-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="8a333-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*Dateiname* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="8a333-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="8a333-115">Der festzulegende Datei Name.</span><span class="sxs-lookup"><span data-stu-id="8a333-115">Filename to set.</span></span> <span data-ttu-id="8a333-116">Der Dateiname kann eine beliebige Kombination von Zeichen sein und muss in doppelte Anführungszeichen ("") eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8a333-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="8a333-117">Wenn dieser Parameter ausgelassen wird, bleibt der vorherige Dateiname unverändert.</span><span class="sxs-lookup"><span data-stu-id="8a333-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a333-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a333-118">Remarks</span></span>

<span data-ttu-id="8a333-119">Der Compiler verwendet die Zeilennummer und den Dateinamen, um auf Fehler zu verweisen, die während der Kompilierung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8a333-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="8a333-120">Die Zeilennummer verweist normalerweise auf die aktuelle Eingabezeile, und der Dateiname verweist auf die aktuelle Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="8a333-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="8a333-121">Nach der Verarbeitung jeder Zeile wird die Zeilennummer erhöht.</span><span class="sxs-lookup"><span data-stu-id="8a333-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="8a333-122">Wenn Sie die Zeilennummer und den Dateinamen ändern, ignoriert der Compiler die vorherigen Werte und setzt die Verarbeitung mit den neuen Werten fort.</span><span class="sxs-lookup"><span data-stu-id="8a333-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="8a333-123">Die \# line-Direktive wird in der Regel von Programm-Generatoren verwendet, damit Fehlermeldungen auf die ursprüngliche Quelldatei und nicht auf das generierte Programm verweisen.</span><span class="sxs-lookup"><span data-stu-id="8a333-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="8a333-124">Der Konvertierer verwendet die Zeilennummer und den Dateinamen, um die Werte der vordefinierten \_ \_ Datei \_ \_ und \_ \_ Zeile \_ \_ der Makros zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8a333-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="8a333-125">Sie können diese Makros verwenden, um selbsterklärende Fehlermeldungen in den Programmtext einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a333-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="8a333-126">Das \_ \_ Datei \_ \_ Makro wird zu einer Zeichenfolge erweitert, deren Inhalt der Dateiname ist, umgeben von doppelten Anführungszeichen ("").</span><span class="sxs-lookup"><span data-stu-id="8a333-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="8a333-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a333-127">Examples</span></span>

<span data-ttu-id="8a333-128">Im folgenden Beispiel wird die Zeilennummer auf 151 und der Dateiname auf "Copy. c" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8a333-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="8a333-129">Im folgenden Beispiel verwendet das Makro Assert die vordefinierte Makros \_ \_ -Zeile \_ \_ und- \_ \_ Datei \_ \_ , um eine Fehlermeldung zur Quelldatei auszugeben, wenn die angegebene Behauptung nicht true ist.</span><span class="sxs-lookup"><span data-stu-id="8a333-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="8a333-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a333-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a333-131">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a333-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





