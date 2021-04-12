---
description: Funktionen, die nicht mit einer Unicode-Version implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Verwenden von Funktionen, die keine Unicode-Entsprechungen aufweisen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218692"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="1fc1a-103">Verwenden von Funktionen, die keine Unicode-Entsprechungen aufweisen</span><span class="sxs-lookup"><span data-stu-id="1fc1a-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="1fc1a-104">Funktionen, die nicht mit einer [Unicode](unicode.md) -Version implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="1fc1a-105">Wenn Sie z. b. Code portieren, der die [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) -Funktion aufruft, kann die Anwendung Unicode unterstützen, indem Sie stattdessen die Funktion "up [**File**](/windows/win32/api/fileapi/nf-fileapi-createfilea) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="1fc1a-106">Wenn eine Funktion keine Unicode-Entsprechung hat, kann die Anwendung vor und nach dem Funktions aufrufzeichen Zeichen aus 8-Bit-Zeichensätzen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="1fc1a-107">Die Zahlen Formatierungsfunktionen " **atoi** " und " **idea** " verwenden z. b. nur die Ziffern 0 bis 9.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="1fc1a-108">Die Zuordnung von Unicode zu 8-Bit-Zeichen führt normalerweise zu Datenverlusten. Dies kann jedoch vermieden werden, indem der Codetyp unabhängig voneinander und die Ausdrücke bedingt werden.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="1fc1a-109">Die Anweisungen im folgenden Beispiel, die für 8-Bit-Zeichen geschrieben wurden, sind typabhängig und sollten geändert werden, damit Unicode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="1fc1a-110">Diese Anweisungen können wie folgt umgeschrieben werden, um Sie typunabhängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="1fc1a-111">In diesem Beispiel übersetzt die Standard-C-Bibliotheksfunktion **wcstomsb** Unicode in ASCII.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="1fc1a-112">Im Beispiel wird davon ausgegangen, dass die Ziffern 0 bis 9 immer aus Unicode in ASCII übersetzt werden können, auch wenn ein Teil des umgebenden Texts nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="1fc1a-113">Die **atoi** -Funktion hält an jedem Zeichen an, das keine Ziffer ist.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="1fc1a-114">Die Anwendung kann die [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) -Funktion der National Language Support (NLS) verwenden, um Text zu verarbeiten, der die systemeigenen [Ziffern](digit-shapes.md) enthält, die für einige der Skripts in Unicode bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="1fc1a-115">Wenn Sie die **wcstomsb** -Funktion falsch verwenden, kann die Sicherheit Ihrer Anwendung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="1fc1a-116">Stellen Sie sicher, dass der Anwendungs Puffer für die Zeichenfolge von 8-Bit-Zeichen mindestens die Größe 2 \* (*Char \_ length* + 1) hat, wobei *Char \_ length* die Länge der Unicode-Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="1fc1a-117">Diese Einschränkung wird vorgenommen, da jedes Unicode-Zeichen mit [Doppelbyte-Zeichensätzen (Double-Byte Character Sets](double-byte-character-sets.md) , dbcss) zwei aufeinander folgenden 8-Bit-Zeichen zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="1fc1a-118">Wenn der Puffer nicht die gesamte Zeichenfolge enthält, wird die Ergebnis Zeichenfolge nicht mit Null beendet und stellt ein Sicherheitsrisiko dar.</span><span class="sxs-lookup"><span data-stu-id="1fc1a-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="1fc1a-119">Weitere Informationen zur Anwendungssicherheit finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="1fc1a-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1fc1a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fc1a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc1a-121">Verwenden von Unicode und Zeichensätzen</span><span class="sxs-lookup"><span data-stu-id="1fc1a-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
