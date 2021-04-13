---
title: import-Attribut
description: Die Import-Direktive gibt eine andere IDL-, ODL-oder Header Datei an, die Definitionen enthält, auf die Sie aus der IDL-Hauptdatei verweisen möchten
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- Import Attribut-Mittel l
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314768"
---
# <a name="import-attribute"></a><span data-ttu-id="82299-104">import-Attribut</span><span class="sxs-lookup"><span data-stu-id="82299-104">import attribute</span></span>

<span data-ttu-id="82299-105">Die **Import** -Direktive gibt eine andere IDL-, ODL-oder Header Datei an, die Definitionen enthält, auf die Sie aus der IDL-Hauptdatei verweisen möchten</span><span class="sxs-lookup"><span data-stu-id="82299-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="82299-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82299-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="82299-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="82299-108">Gibt den Namen der zu importierenden Header-, IDL-oder ODL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="82299-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82299-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82299-109">Remarks</span></span>

<span data-ttu-id="82299-110">Mit der **Import** -Direktive werden alle IDL-Anweisungen in der importierten Datei (z. b. Typedefs, Konstante Deklarationen und Schnittstellendefinitionen) für den Import verfügbar. IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82299-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="82299-111">Die importierte Datei wird separat verarbeitet (d. h., dass der CPP-Präprozessor unabhängig aufgerufen wird) aus der importierenden IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82299-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="82299-112">Auf diese Weise führen Präprozessordirektiven, wie z. b. \# define, nicht aus einer importierten Header-oder IDL-Datei in die importierende IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="82299-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="82299-113">Wie das Präprozessormakro in der C-Sprache weist die **Import** -Direktive den Compiler an, Datentypen einzuschließen, die in den importierten IDL-Dateien definiert wurden. **\#**</span><span class="sxs-lookup"><span data-stu-id="82299-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="82299-114">Anders als bei der **\# include** -Direktive ignoriert die **Import** -Direktive Prozedur Prototypen, da für Elemente in der importierten Datei keine Stubdaten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="82299-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="82299-115">Spezifische Informationen zum Verwenden von **Import** zum Einschließen von Header Dateien in eine IDL-Datei finden Sie unter [Importieren von System Header Dateien](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="82299-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="82299-116">Der C-sprach Header (. H) die für die Schnittstelle generierte Datei enthält nicht direkt die importierten Typen, sondern generiert stattdessen eine **\# include** -Direktive für die Header Datei, die der importierten Schnittstelle entspricht.</span><span class="sxs-lookup"><span data-stu-id="82299-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="82299-117">Dies ist beispielsweise der Fall, wenn Sie Base importieren. IDL in Ihre abgeleitete. IDL, die generierte Header Datei, die abgeleitet wurde. H enthält die Direktive **\# include** Base. h.</span><span class="sxs-lookup"><span data-stu-id="82299-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="82299-118">Es gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="82299-118">The following rules apply:</span></span>

-   <span data-ttu-id="82299-119">Das **Import** -Schlüsselwort ist optional und kann in der IDL-Datei null oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="82299-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="82299-120">Jedem **Import** Schlüsselwort können mehr als ein Dateiname zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="82299-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="82299-121">Trennen Sie mehrere Dateinamen durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="82299-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="82299-122">Sie müssen den Dateinamen in Anführungszeichen einschließen und die Import Anweisung mit einem Semikolon (;)) beenden.</span><span class="sxs-lookup"><span data-stu-id="82299-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="82299-123">Sie können eine Schnittstelle, die über keine Attribute verfügt, in eine andere IDL-Datei importieren.</span><span class="sxs-lookup"><span data-stu-id="82299-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="82299-124">Die Schnittstelle darf jedoch nur Datentypen enthalten. Er darf keine Prozeduren enthalten.</span><span class="sxs-lookup"><span data-stu-id="82299-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="82299-125">Wenn auch eine Prozedur in der importierten Schnittstelle enthalten ist, müssen Sie ein [**Lokales**](local.md) Attribut oder ein [**UUID**](uuid.md) -Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="82299-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="82299-126">Die **Import** Funktion ist idemtypfähig. das heißt, dass das Importieren einer Schnittstelle mehr als einmal keine weiteren Auswirkungen hat.</span><span class="sxs-lookup"><span data-stu-id="82299-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="82299-127">Das Verhalten der **Import** Direktive ist unabhängig von den [**/MS \_ ext**](-ms-ext.md) (Standard), [**/OSF**](-osf.md)und [**/App \_**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="82299-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="82299-128">Der Compilermodus (**/OSF** oder **/MS \_ ext**) kann sich jedoch auf die Zeiger Attribut Ergänzung für importierte Typen auswirken.</span><span class="sxs-lookup"><span data-stu-id="82299-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="82299-129">Weitere Informationen finden Sie unter [Pointer-Attribute Type-Vererbung](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="82299-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="82299-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82299-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="82299-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82299-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82299-132">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="82299-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="82299-133">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="82299-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="82299-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="82299-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="82299-135">**darunter**</span><span class="sxs-lookup"><span data-stu-id="82299-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="82299-136">Importieren von System-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="82299-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="82299-137">Importieren von Dateien und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="82299-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="82299-138">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="82299-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="82299-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="82299-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 