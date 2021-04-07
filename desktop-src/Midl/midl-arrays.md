---
title: Mittelgroße Arrays
description: Mittel l-Arrays.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- Datentypen mittlerer l, Arrays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038935"
---
# <a name="midl-arrays"></a><span data-ttu-id="656d1-104">Mittelgroße Arrays</span><span class="sxs-lookup"><span data-stu-id="656d1-104">MIDL Arrays</span></span>

<span data-ttu-id="656d1-105">Arraydeklaratoren werden im Schnittstellen Text der IDL-Datei als einer der folgenden Zeichen folgen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="656d1-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="656d1-106">Teil einer allgemeinen Deklaration</span><span class="sxs-lookup"><span data-stu-id="656d1-106">Part of a general declaration</span></span>
-   <span data-ttu-id="656d1-107">Ein Member einer Struktur oder eines Union-Deklarators.</span><span class="sxs-lookup"><span data-stu-id="656d1-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="656d1-108">Ein Parameter für einen Remote Prozedur aufrufen</span><span class="sxs-lookup"><span data-stu-id="656d1-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="656d1-109">Die Begrenzungen der einzelnen Dimensionen des Arrays werden innerhalb eines separaten Paars von eckigen Klammern ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="656d1-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="656d1-110">Ein Ausdruck, der zu *n* ausgewertet wird, steht für eine untere Grenze von 0 (null) und eine obere Grenze von *n-1*.</span><span class="sxs-lookup"><span data-stu-id="656d1-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="656d1-111">Wenn die eckigen Klammern leer sind oder ein einzelnes Sternchen ( \* ) enthalten, ist die untere Grenze NULL, und die obere Grenze wird zur Laufzeit bestimmt.</span><span class="sxs-lookup"><span data-stu-id="656d1-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="656d1-112">Das Array kann auch zwei durch ein Auslassungs Zeichen getrennte Werte enthalten, die die unteren und oberen Begrenzungen des Arrays darstellen, wie in \[ *niedriger*... *oben* \] .</span><span class="sxs-lookup"><span data-stu-id="656d1-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="656d1-113">Microsoft RPC erfordert eine untere Grenze von NULL.</span><span class="sxs-lookup"><span data-stu-id="656d1-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="656d1-114">Der mittlerer l-Compiler erkennt keine Konstrukte, die niedrigere Grenzen ungleich NULL angeben.</span><span class="sxs-lookup"><span data-stu-id="656d1-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="656d1-115">Arrays können den Feld Attributen "size", " [**Max \_ is**](max-is.md)", " [**length \_ is**](length-is.md)", " [**First \_ is**](first-is.md)" und " [**Last" \_ ist**](last-is.md) die Angabe der Größe des Arrays oder des Teils des Arrays, das gültige Daten enthält. [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="656d1-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="656d1-116">Diese Feld Attribute identifizieren den Parameter, das Strukturfeld oder die Konstante, die die Array Dimension oder den Index angibt.</span><span class="sxs-lookup"><span data-stu-id="656d1-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="656d1-117">Das Array muss mit dem Bezeichner verknüpft werden, der vom Feld Attribut auf folgende Weise angegeben wird: Wenn das Array ein Parameter ist, muss der Bezeichner auch ein Parameter für dieselbe Funktion sein. Wenn das Array ein Strukturfeld ist, muss der Bezeichner ein weiteres Strukturfeld derselben Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="656d1-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="656d1-118">Ein Array wird als "konform" bezeichnet, wenn die obere Grenze einer Dimension zur Laufzeit bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="656d1-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="656d1-119">(Nur obere Begrenzungen können zur Laufzeit bestimmt werden.) Um die obere Grenze zu ermitteln, muss die Array Deklaration [**eine \_ Größe**](size-is.md) oder ein [**Maximales \_ is**](max-is.md) -Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="656d1-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="656d1-120">Ein Array wird als "Variation" bezeichnet, wenn seine Begrenzungen zur Kompilierzeit bestimmt werden, der Bereich der übertragenen Elemente jedoch zur Laufzeit bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="656d1-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="656d1-121">Um den Bereich der übertragenen Elemente zu ermitteln, muss die Array Deklaration [**eine \_ Länge**](length-is.md)von, [**First \_ ist**](first-is.md)oder das [**Letzte \_ is**](last-is.md) -Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="656d1-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="656d1-122">Ein Übereinstimmung unterschiedliches Array (auch als "Open" bezeichnet) ist ein Array, dessen obere Grenze und der Bereich der übertragenen Elemente zur Laufzeit bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="656d1-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="656d1-123">Höchstens ein konformes oder konform veränderliches Array kann in eine C-Struktur eingefügt werden und muss das letzte Element der Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="656d1-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="656d1-124">Im Gegensatz dazu können nicht konforme Arrays an beliebiger Stelle in einer Struktur vorkommen.</span><span class="sxs-lookup"><span data-stu-id="656d1-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="656d1-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="656d1-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="656d1-126">Weitere Informationen finden Sie unter [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="656d1-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="656d1-127">Mehrdimensionale Arrays</span><span class="sxs-lookup"><span data-stu-id="656d1-127">Multidimensional Arrays</span></span>

<span data-ttu-id="656d1-128">Der Benutzer kann Typen deklarieren, die Arrays sind, und dann Arrays von Objekten dieser Typen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="656d1-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="656d1-129">Die Semantik von *m*-dimensionalen Arrays von *n*-dimensionalen Array Typen ist mit der Semantik von *m* + *n*-dimensionalen Arrays identisch.</span><span class="sxs-lookup"><span data-stu-id="656d1-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="656d1-130">Beispielsweise kann der Typ "Rect" \_ als zweidimensionales Array definiert werden, und die Variable " *Rect* " kann als ein Array vom Typ "Rect" definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="656d1-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="656d1-131">Dies entspricht dem dreidimensionalen Array *Äquivalent " \_ Rect*":</span><span class="sxs-lookup"><span data-stu-id="656d1-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="656d1-132">Microsoft RPC ist C-orientiert.</span><span class="sxs-lookup"><span data-stu-id="656d1-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="656d1-133">Gemäß den Konventionen der C-Sprache kann nur die erste Dimension eines mehrdimensionalen Arrays zur Laufzeit bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="656d1-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="656d1-134">Die Interoperation mit DCE-IDL-Arrays, die andere Sprachen unterstützen, ist auf Folgendes beschränkt:</span><span class="sxs-lookup"><span data-stu-id="656d1-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="656d1-135">Mehrdimensionale Arrays mit Konstanten (Kompilierzeit festgelegten) Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="656d1-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="656d1-136">Mehrdimensionale Arrays mit allen Konstanten Begrenzungen außer der ersten Dimension.</span><span class="sxs-lookup"><span data-stu-id="656d1-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="656d1-137">Die obere Grenze und der Bereich der übertragenen Elemente der ersten Dimension sind von der Laufzeit abhängig.</span><span class="sxs-lookup"><span data-stu-id="656d1-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="656d1-138">Alle eindimensionalen Arrays mit einer unteren Grenze von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="656d1-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="656d1-139">Wenn das **\[** [**String**](string.md) - **\]** Attribut für mehrdimensionale Arrays verwendet wird, gilt das-Attribut für das äußteste ganz rechts.</span><span class="sxs-lookup"><span data-stu-id="656d1-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="656d1-140">Arrays von Zeigern</span><span class="sxs-lookup"><span data-stu-id="656d1-140">Arrays of Pointers</span></span>

<span data-ttu-id="656d1-141">Verweis Zeiger müssen auf gültige Daten zeigen.</span><span class="sxs-lookup"><span data-stu-id="656d1-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="656d1-142">Die Client Anwendung muss den gesamten Arbeitsspeicher für ein **\[** [**in**](in.md) - **\]** oder **\[** **in-,**[**out**](out-idl.md) - **\]** Array von Verweis Zeigern zuordnen, insbesondere wenn das Array mit den Werten **\[ in \]**, oder **\[** **in, out \]**, **\[** [**length \_ is**](length-is.md) **\]** oder **\[** [**Last \_ is**](last-is.md) **\]** zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="656d1-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="656d1-143">Die Client Anwendung muss auch alle Array Elemente vor dem-Befehl initialisieren.</span><span class="sxs-lookup"><span data-stu-id="656d1-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="656d1-144">Vor der Rückgabe an den Client muss die Serveranwendung überprüfen, ob alle Array Elemente im übertragenen Bereich auf einen gültigen Speicher zeigen.</span><span class="sxs-lookup"><span data-stu-id="656d1-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="656d1-145">Auf der Serverseite ordnet der Stub Speicher für alle Array Elemente zu, unabhängig davon, wie **\[** [**lange \_**](length-is.md) der **\]** Wert ist oder der **\[** letzte Wert zum Zeitpunkt des [**\_ Aufrufes ist**](last-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="656d1-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="656d1-146">Diese Funktion kann sich auf die Leistung Ihrer Anwendung auswirken.</span><span class="sxs-lookup"><span data-stu-id="656d1-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="656d1-147">Es gelten keine Einschränkungen für Arrays eindeutiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="656d1-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="656d1-148">Sowohl auf dem Client als auch auf dem Server wird der Speicher für NULL-Zeiger zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="656d1-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="656d1-149">Wenn Zeiger ungleich NULL sind, werden die Daten in einem vorab zugeordneten Speicher abgelegt.</span><span class="sxs-lookup"><span data-stu-id="656d1-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="656d1-150">Ein optionaler zeigerdeklarator kann dem Arraydeklarator vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="656d1-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="656d1-151">Wenn eingebettete Verweis Zeiger reine **\[** [**out**](out-idl.md) **\]** -Parameter sind, muss der Server-Manager-Code dem Array von Verweis Zeigern gültige Werte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="656d1-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="656d1-152">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="656d1-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="656d1-153">Die generierten stubwerte ordnen das Array zu und weisen allen in das Array eingebetteten Zeigern NULL-Werte zu.</span><span class="sxs-lookup"><span data-stu-id="656d1-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 