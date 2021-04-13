---
title: Die Tools
description: In diesem Thema werden die Tools beschrieben, die Sie bei der Verwendung von bereitstellen können, um Ihre 64 Anwendung zu erstellen. Windows 10 ist für x64-und ARM64-basierte Prozessoren verfügbar.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Tools
- Tools 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388599"
---
# <a name="the-tools"></a><span data-ttu-id="865cc-106">Die Tools</span><span class="sxs-lookup"><span data-stu-id="865cc-106">The Tools</span></span>

<span data-ttu-id="865cc-107">In diesem Thema werden die Tools beschrieben, die Sie bei der Verwendung von bereitstellen können, um Ihre 64 Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="865cc-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="865cc-108">Windows 10 ist für x64-und ARM64-basierte Prozessoren verfügbar.</span><span class="sxs-lookup"><span data-stu-id="865cc-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="865cc-109">Includedateien</span><span class="sxs-lookup"><span data-stu-id="865cc-109">Include Files</span></span>

<span data-ttu-id="865cc-110">Die API-Elemente sind zwischen 32-und 64-Bit-Fenstern praktisch identisch.</span><span class="sxs-lookup"><span data-stu-id="865cc-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="865cc-111">Die Windows-Header Dateien wurden so geändert, dass Sie sowohl für 32-als auch für 64-Bit-Code verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="865cc-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="865cc-112">Die neuen 64-Bit-Typen und-Makros werden in der neuen Header Datei "basetsd. h" definiert, die sich im Satz der in Windows. h enthaltenen Header Dateien befindet.</span><span class="sxs-lookup"><span data-stu-id="865cc-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="865cc-113">Basetsd. h enthält die neuen Datentyp Definitionen zur Unterstützung bei der Kenn Wort Größe des Quellcodes.</span><span class="sxs-lookup"><span data-stu-id="865cc-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="865cc-114">Neue Datentypen</span><span class="sxs-lookup"><span data-stu-id="865cc-114">New Data Types</span></span>

<span data-ttu-id="865cc-115">Die Windows-Header Dateien enthalten neue Datentypen.</span><span class="sxs-lookup"><span data-stu-id="865cc-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="865cc-116">Diese Typen sind in erster Linie für die Typkompatibilität mit den 32-Bit-Datentypen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="865cc-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="865cc-117">Die neuen Typen bieten genau dieselbe Typisierung wie die vorhandenen Typen, während gleichzeitig die Unterstützung für die 64-Bit-Windows-Bereitstellung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="865cc-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="865cc-118">Weitere Informationen finden Sie in [den neuen Datentypen](the-new-data-types.md) oder in der Header Datei "basetsd. h".</span><span class="sxs-lookup"><span data-stu-id="865cc-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="865cc-119">Vordefinierte Makros</span><span class="sxs-lookup"><span data-stu-id="865cc-119">Predefined Macros</span></span>

<span data-ttu-id="865cc-120">Der Compiler definiert die folgenden Makros, um die Plattform zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="865cc-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="865cc-121">Makro</span><span class="sxs-lookup"><span data-stu-id="865cc-121">Macro</span></span>   | <span data-ttu-id="865cc-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="865cc-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865cc-123">\_Win64</span><span class="sxs-lookup"><span data-stu-id="865cc-123">\_WIN64</span></span> | <span data-ttu-id="865cc-124">Eine 64-Bit-Plattform.</span><span class="sxs-lookup"><span data-stu-id="865cc-124">A 64-bit platform.</span></span> <span data-ttu-id="865cc-125">Dies schließt sowohl x64 als auch ARM64 ein.</span><span class="sxs-lookup"><span data-stu-id="865cc-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="865cc-126">\_Win32</span><span class="sxs-lookup"><span data-stu-id="865cc-126">\_WIN32</span></span> | <span data-ttu-id="865cc-127">Eine 32-Bit-Plattform.</span><span class="sxs-lookup"><span data-stu-id="865cc-127">A 32-bit platform.</span></span> <span data-ttu-id="865cc-128">Dieser Wert wird auch vom 64-Bit-Compiler aus Gründen der Abwärtskompatibilität definiert.</span><span class="sxs-lookup"><span data-stu-id="865cc-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="865cc-129">\_Win16</span><span class="sxs-lookup"><span data-stu-id="865cc-129">\_WIN16</span></span> | <span data-ttu-id="865cc-130">Eine 16-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="865cc-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="865cc-131">Die folgenden Makros sind spezifisch für die-Architektur.</span><span class="sxs-lookup"><span data-stu-id="865cc-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="865cc-132">Makro</span><span class="sxs-lookup"><span data-stu-id="865cc-132">Macro</span></span>      | <span data-ttu-id="865cc-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="865cc-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="865cc-134">\_M \_ ia64</span><span class="sxs-lookup"><span data-stu-id="865cc-134">\_M\_IA64</span></span>  | <span data-ttu-id="865cc-135">Intel Itanium-Plattform</span><span class="sxs-lookup"><span data-stu-id="865cc-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="865cc-136">\_M \_ IX86</span><span class="sxs-lookup"><span data-stu-id="865cc-136">\_M\_IX86</span></span>  | <span data-ttu-id="865cc-137">x86-Plattform</span><span class="sxs-lookup"><span data-stu-id="865cc-137">x86 platform</span></span>           |
| <span data-ttu-id="865cc-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="865cc-138">\_M\_X64</span></span>   | <span data-ttu-id="865cc-139">x64-Plattform</span><span class="sxs-lookup"><span data-stu-id="865cc-139">x64 platform</span></span>           |
| <span data-ttu-id="865cc-140">\_M \_ ARM64</span><span class="sxs-lookup"><span data-stu-id="865cc-140">\_M\_ARM64</span></span> | <span data-ttu-id="865cc-141">ARM64-Plattform</span><span class="sxs-lookup"><span data-stu-id="865cc-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="865cc-142">Verwenden Sie diese Makros nicht nur mit Architektur spezifischem Code, sondern verwenden Sie stattdessen \_ Win64, \_ Win32 und \_ Win16, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="865cc-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="865cc-143">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="865cc-143">Helper Functions</span></span>

<span data-ttu-id="865cc-144">Die folgenden Inline Funktionen (in basetsd. h definiert) können Ihnen helfen, Werte problemlos von einem Typ in einen anderen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="865cc-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="865cc-145">**Inttoptr** signiert den **int** -Wert, **uinttoptr** NULL erweitert den ganzzahligen **int** -Wert, **longtoptr** signiert den **Long** -Wert, und **ulongtoptr** NULL erweitert den Long-Wert **ohne** Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="865cc-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="865cc-146">64-Bit-Compiler</span><span class="sxs-lookup"><span data-stu-id="865cc-146">64-bit Compiler</span></span>

<span data-ttu-id="865cc-147">Die 64-Bit-Compiler können verwendet werden, um Zeiger abkürzen, falsche Typumwandlungen und andere 64-Bit-spezifische Probleme zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="865cc-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="865cc-148">Wenn der Compiler zum ersten Mal ausgeführt wird, generiert er wahrscheinlich viele Zeiger abkürzen oder Typen Konflikt Warnungen, wie z. b. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="865cc-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="865cc-149">Verwenden Sie diese Warnungen als Leitfaden, um den Code stabiler zu machen.</span><span class="sxs-lookup"><span data-stu-id="865cc-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="865cc-150">Es empfiehlt sich, alle Warnungen zu eliminieren, insbesondere Warnungen für Zeiger abkürzen.</span><span class="sxs-lookup"><span data-stu-id="865cc-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="865cc-151">64-Bit-Compilerschalter und-Warnungen</span><span class="sxs-lookup"><span data-stu-id="865cc-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="865cc-152">Beachten Sie, dass dieser Compiler das LLP64-Datenmodell aktiviert.</span><span class="sxs-lookup"><span data-stu-id="865cc-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="865cc-153">Es gibt eine Warn Option, die das Portieren von LLP64 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="865cc-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="865cc-154">Der Schalter-Wp64-w3 aktiviert die folgenden Warnungen:</span><span class="sxs-lookup"><span data-stu-id="865cc-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="865cc-155">C4305: trunationwarnung.</span><span class="sxs-lookup"><span data-stu-id="865cc-155">C4305: Truncation warning.</span></span> <span data-ttu-id="865cc-156">Beispiel: "Return": Abschneiden von "unsigned Int64" in "Long".</span><span class="sxs-lookup"><span data-stu-id="865cc-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="865cc-157">C4311: trunationwarnung.</span><span class="sxs-lookup"><span data-stu-id="865cc-157">C4311: Truncation warning.</span></span> <span data-ttu-id="865cc-158">Beispiel: "Typumwandlung": Zeiger Verkürzung von "int \* \_ ptr64" in "int".</span><span class="sxs-lookup"><span data-stu-id="865cc-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="865cc-159">C4312: Konvertierung in eine größere warnungsgrößenwarnung.</span><span class="sxs-lookup"><span data-stu-id="865cc-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="865cc-160">Beispiel: "Typumwandlung": Konvertierung von "int" in "int \* \_ ptr64" von größerer Größe.</span><span class="sxs-lookup"><span data-stu-id="865cc-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="865cc-161">C4318: Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="865cc-161">C4318: Passing zero length.</span></span> <span data-ttu-id="865cc-162">Übergeben Sie z. b. Konstante NULL als Länge an die **memset** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="865cc-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="865cc-163">C4319: Not-Operator.</span><span class="sxs-lookup"><span data-stu-id="865cc-163">C4319: Not operator.</span></span> <span data-ttu-id="865cc-164">Beispiel: "~": keine Erweiterung von "unsigned long" in "unsigned \_ Int64" von größerer Größe.</span><span class="sxs-lookup"><span data-stu-id="865cc-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="865cc-165">C4313: Aufrufen der **printf** -Funktions Familie mit in Konflikt stehenden konvertierungstypspezifizierer und-Argumenten.</span><span class="sxs-lookup"><span data-stu-id="865cc-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="865cc-166">Beispielsweise steht "printf": "% p" in der Format Zeichenfolge in Konflikt mit Argument 2 vom Typ " \_ Int64".</span><span class="sxs-lookup"><span data-stu-id="865cc-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="865cc-167">Ein weiteres Beispiel ist der callf-Ausdruck ("% x", Zeiger \_ Wert). Dies bewirkt, dass die oberen 32 Bits abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="865cc-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="865cc-168">Der richtige-Rückruf ist printf ("% p", Zeiger \_ Wert).</span><span class="sxs-lookup"><span data-stu-id="865cc-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="865cc-169">C4244: identisch mit der vorhandenen Warnung C4242.</span><span class="sxs-lookup"><span data-stu-id="865cc-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="865cc-170">Beispiel: "Return": Konvertierung von " \_ Int64" in "unsigned int", möglicher Datenverlust.</span><span class="sxs-lookup"><span data-stu-id="865cc-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="865cc-171">64-Bit-Linker und-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="865cc-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="865cc-172">Verwenden Sie zum Erstellen von Anwendungen den Linker und die Bibliotheken, die von der Windows SDK bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="865cc-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="865cc-173">Die meisten 32-Bit-Bibliotheken verfügen über eine entsprechende 64-Bit-Version, aber bestimmte Legacy Bibliotheken sind nur in 32-Bit-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="865cc-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="865cc-174">Code, der diese Bibliotheken aufruft, kann nicht verknüpft werden, wenn die Anwendung für 64-Bit-Windows erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="865cc-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





