---
title: Das Zeichen folgen Attribut in Arrays
description: Sie können das Attribut \ String \ für eindimensionale Zeichen Arrays, breit Zeichen Arrays und Byte Arrays verwenden, die Text Zeichenfolgen darstellen.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102003"
---
# <a name="the-string-attribute-in-arrays"></a><span data-ttu-id="b436b-104">Das \[ Zeichen folgen \] Attribut in Arrays</span><span class="sxs-lookup"><span data-stu-id="b436b-104">The \[string\] Attribute in Arrays</span></span>

<span data-ttu-id="b436b-105">Sie können das \[ [String](/windows/desktop/Midl/string) - \] Attribut für eindimensionale Zeichen Arrays, breit Zeichen Arrays und Byte Arrays verwenden, die Text Zeichenfolgen darstellen.</span><span class="sxs-lookup"><span data-stu-id="b436b-105">You can use the \[ [string](/windows/desktop/Midl/string)\] attribute for one-dimensional character arrays, wide-character arrays, and byte arrays that represent text strings.</span></span> <span data-ttu-id="b436b-106">Wenn Sie das **\[ \] Zeichen** folgen Attribut verwenden, verwendet der Clientstub die C-Bibliotheksfunktionen von " **straulen** " oder " **wstrinlen** ", um die Anzahl der Zeichen in der Zeichenfolge zu zählen.</span><span class="sxs-lookup"><span data-stu-id="b436b-106">If you use the **\[string\]** attribute, the client stub uses the C-library functions **strlen** or **wstrlen** to count the number of characters in the string.</span></span> <span data-ttu-id="b436b-107">Um mögliche Inkonsistenzen zu vermeiden, können Sie das **\[ Zeichen \]** folgen Attribut nicht zur gleichen Zeit wie die \[ [erste \_ is](/windows/desktop/Midl/first-is) \] -, \[ [Last \_](/windows/desktop/Midl/last-is) \] -und \[ [size \_](/windows/desktop/Midl/size-is) - \] Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="b436b-107">To avoid possible inconsistencies, MIDL does not let you use the **\[string\]** attribute at the same time as the \[ [first\_is](/windows/desktop/Midl/first-is)\], \[ [last\_is](/windows/desktop/Midl/last-is)\], and \[ [size\_is](/windows/desktop/Midl/size-is)\] attributes.</span></span>

<span data-ttu-id="b436b-108">Bei null-terminierten Zeichen folgen in C müssen Sie Leerzeichen für das NULL Zeichen am Ende der Zeichenfolge zulassen.</span><span class="sxs-lookup"><span data-stu-id="b436b-108">With null-terminated strings in C, you must allow space for the null character at the end of the string.</span></span> <span data-ttu-id="b436b-109">Wenn Sie z. b. eine Zeichenfolge mit bis zu 80 Zeichen deklarieren, müssen Sie 81 Zeichen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b436b-109">For example, when declaring a string that will hold up to 80 characters, allocate 81 characters.</span></span> <span data-ttu-id="b436b-110">Die folgende Beispiel-IDL-Datei veranschaulicht das Deklarieren von Arrays mit dem **\[ Zeichen \]** folgen Attribut.</span><span class="sxs-lookup"><span data-stu-id="b436b-110">The following sample IDL file demonstrates how to declare arrays with the **\[string\]** attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 