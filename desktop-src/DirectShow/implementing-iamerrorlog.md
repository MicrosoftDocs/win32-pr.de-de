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
# <a name="implementing-iamerrorlog"></a>Implementieren von iamerrorlog

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle enthält eine einzelne Methode, [**LogError**](iamerrorlog-logerror.md). Die Parameter für die-Methode enthalten Informationen zum aufgetretenen Fehler.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Der Fehlercode und die Fehler Zeichenfolge werden durch DirectShow-Bearbeitungs Dienste definiert. Eine Liste der Fehler finden Sie unter [Rendern von Fehlern](rendering-errors.md).

Der *pextrainfo* -Parameter enthält einen Zeiger auf einen Variant-Typ, der zusätzliche Informationen über den Fehler enthält. Der Datentyp und der Inhalt der Variante sind abhängig von dem spezifischen Fehler, der aufgetreten ist. Wenn der Fehler z. b. durch einen falschen Dateinamen verursacht wurde, ist die Variante eine Zeichenfolge mit dem ungültigen Dateinamen. Einige Fehler enthalten keine zusätzlichen Informationen, daher kann *pextrainfo* **null** sein. Der folgende Code zeigt, wie Sie das **VT** -Element der Variante, die den Datentyp angibt, testen und eine Nachricht entsprechend formatieren.


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
> Gibt die Variante nicht frei, auf die verweist.
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
> . Außerdem wird die Variante nach dem zurückkehren der Methode ungültig, sodass Sie später nicht darauf verweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungs Fehler](logging-errors.md)
</dt> </dl>

 

 



