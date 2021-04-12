---
title: Übersetzen in Java aus C++
description: Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird. Speicher Zeiger bieten diesen direkten Zugriff. In Java werden Zeiger für Sie behandelt.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388022"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="b3493-105">Übersetzen in Java aus C++</span><span class="sxs-lookup"><span data-stu-id="b3493-105">Translating to Java from C++</span></span>

<span data-ttu-id="b3493-106">Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b3493-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="b3493-107">Speicher Zeiger bieten diesen direkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="b3493-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="b3493-108">In Java werden Zeiger für Sie behandelt.</span><span class="sxs-lookup"><span data-stu-id="b3493-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="b3493-109">In Java werden zusammengesetzte Datentypen " **struct**", " **Union**" und " **typedef** " ausschließlich durch die Verwendung von Klassen behandelt.</span><span class="sxs-lookup"><span data-stu-id="b3493-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="b3493-110">Der Datentyp C++ **Variant** ist beispielsweise com. **ms. com. Variant** in Java zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b3493-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="b3493-111">In C++ sind Zeichen folgen ein Zeichen Array.</span><span class="sxs-lookup"><span data-stu-id="b3493-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="b3493-112">In Java sind Zeichen folgen Objekte.</span><span class="sxs-lookup"><span data-stu-id="b3493-112">In Java, strings are objects.</span></span> <span data-ttu-id="b3493-113">Methoden, die auf Zeichen folgen reagieren, behandeln die Zeichenfolge als ein ganzes Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3493-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="b3493-114">COM-Methoden geben einen als **HRESULT** bezeichneten Wert zurück, bei dem es sich um einen 32-Bit-Fehlercode handelt.</span><span class="sxs-lookup"><span data-stu-id="b3493-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="b3493-115">Die Java-Unterstützung für Microsoft Internet Explorer definiert die Klasse **com. ms. com. COMException**, die den **HRESULT** -Fehlercode umschließt.</span><span class="sxs-lookup"><span data-stu-id="b3493-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="b3493-116">Java unterstützt keine unsignierten Datentypen mit Ausnahme von **char**, eine 16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b3493-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="b3493-117">Methoden, die andere nicht signierte Datentypen akzeptieren oder zurückgeben, können nicht in Java verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3493-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="b3493-118">Java unterstützt keine mehrdimensionalen Arrays.</span><span class="sxs-lookup"><span data-stu-id="b3493-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="b3493-119">Methoden, die mehrdimensionale Arrays akzeptieren oder zurückgeben, sind von Java aus nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b3493-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="b3493-120">Boolesche Werte in Java können nicht in 0 und 1 umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b3493-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3493-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3493-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3493-122">Übersetzen in Java</span><span class="sxs-lookup"><span data-stu-id="b3493-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




