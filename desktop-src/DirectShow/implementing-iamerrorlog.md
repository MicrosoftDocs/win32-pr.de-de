---
description: Implementieren von IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementieren von IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378d48ec9047da6068e8d95143f8b10b7016faea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465237"
---
# <a name="implementing-iamerrorlog"></a>Implementieren von IAMErrorLog

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Die [**IAMErrorLog-Schnittstelle**](iamerrorlog.md) enthält eine einzelne Methode, [**LogError.**](iamerrorlog-logerror.md) Die Parameter der -Methode enthalten Informationen zum aufgetretenen Fehler.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



Der Fehlercode und die Fehlerzeichenfolge werden von DirectShow Editing Services definiert. Eine Liste der Fehler finden Sie unter [Renderingfehler.](rendering-errors.md)

Der *pExtraInfo-Parameter* enthält einen Zeiger auf einen VARIANT-Typ, der zusätzliche Informationen zum Fehler enthält. Der Datentyp und der Inhalt der VARIANT-Datei hängen vom spezifischen Aufgetretenen Fehler ab. Wenn der Fehler beispielsweise durch einen falschen Dateinamen verursacht wurde, ist variant eine Zeichenfolge mit dem ungültigen Dateinamen. Einige Fehler enthalten keine zusätzlichen Informationen, sodass *pExtraInfo* möglicherweise **NULL ist.** Der folgende Code zeigt, wie sie den **vt-Member** der VARIANT-Datei testen, die den Datentyp angibt, und eine Meldung entsprechend formatieren.


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
> Geben Sie den VARIANT-Wert, auf den zeigt, nicht frei.
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . Außerdem wird der VARIANT-Wert ungültig, nachdem die Methode zurückgegeben wurde. Verweisen Sie daher später nicht darauf.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungsfehler](logging-errors.md)
</dt> </dl>

 

 



