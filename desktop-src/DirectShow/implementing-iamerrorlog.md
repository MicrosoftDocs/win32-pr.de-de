---
description: Implementieren von iamerrorlog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementieren von iamerrorlog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343140"
---
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="030c0-103">Implementieren von iamerrorlog</span><span class="sxs-lookup"><span data-stu-id="030c0-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="030c0-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="030c0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="030c0-105">Die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle enthält eine einzelne Methode, [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="030c0-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="030c0-106">Die Parameter für die-Methode enthalten Informationen zum aufgetretenen Fehler.</span><span class="sxs-lookup"><span data-stu-id="030c0-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="030c0-107">Der Fehlercode und die Fehler Zeichenfolge werden durch DirectShow-Bearbeitungs Dienste definiert.</span><span class="sxs-lookup"><span data-stu-id="030c0-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="030c0-108">Eine Liste der Fehler finden Sie unter [Rendern von Fehlern](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="030c0-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="030c0-109">Der *pextrainfo* -Parameter enthält einen Zeiger auf einen Variant-Typ, der zusätzliche Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="030c0-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="030c0-110">Der Datentyp und der Inhalt der Variante sind abhängig von dem spezifischen Fehler, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="030c0-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="030c0-111">Wenn der Fehler z. b. durch einen falschen Dateinamen verursacht wurde, ist die Variante eine Zeichenfolge mit dem ungültigen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="030c0-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="030c0-112">Einige Fehler enthalten keine zusätzlichen Informationen, daher kann *pextrainfo* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="030c0-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="030c0-113">Der folgende Code zeigt, wie Sie das **VT** -Element der Variante, die den Datentyp angibt, testen und eine Nachricht entsprechend formatieren.</span><span class="sxs-lookup"><span data-stu-id="030c0-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> <span data-ttu-id="030c0-114">Gibt die Variante nicht frei, auf die verweist.</span><span class="sxs-lookup"><span data-stu-id="030c0-114">Do not free the VARIANT pointed to by</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="030c0-115">.</span><span class="sxs-lookup"><span data-stu-id="030c0-115">.</span></span> <span data-ttu-id="030c0-116">Außerdem wird die Variante nach dem zurückkehren der Methode ungültig, sodass Sie später nicht darauf verweisen.</span><span class="sxs-lookup"><span data-stu-id="030c0-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="030c0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="030c0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030c0-118">Protokollierungs Fehler</span><span class="sxs-lookup"><span data-stu-id="030c0-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



