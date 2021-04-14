---
description: Übersicht über die com-Bibliothek und Hinweise zur Verwendung von Tablet PC-Technologie Abschnitten des Windows Vista SDK.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Verwenden der com-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343279"
---
# <a name="using-the-com-library"></a>Verwenden der com-Bibliothek

Die Referenz zur Tablet PC-verwalteten Bibliothek finden Sie im Abschnitt "reguläre Referenz zur Windows Vista SDK-Klassenbibliothek". Sie stellt ein Objektmodell für Microsoft Visual C++ bereit. Die Mehrzahl der Objekte in der com-Bibliothek sind identisch mit denen in der von Tablet PC verwalteten API.

Die com-API enthält jedoch einige Mitglieder zusätzlich zu den in der verwalteten API gefundenen Membern aufgrund von Unterschieden zwischen der standardmäßigen Microsoft Win32-Umgebung und der Microsoft .net frameworksoftware Development Kit (SDK)-Umgebung. Beispielsweise werden die Objekte inkrechteck und inktransform in com verwendet, das FrameworkSDK bietet jedoch eine native Implementierung für die [**inkrechteck-Klasse**](inkrectangle-class.md) und die [**inktransform-Klasse**](inktransform-class.md) , die die Notwendigkeit dieser Objekte in der von Tablet PC Platform verwalteten API entfällt.

> [!Note]  
> Die Objekte in der com-API und den Freihand-Steuerelementen sind nicht für die Verwendung in ASP (Active Server Pages) konzipiert.

 

## <a name="working-with-collections"></a>Arbeiten mit Sammlungen

Wenn Sie einen **null** -Wert als Index an eine der Auflistungs Objekte in der com-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argument Werte bei der Erstellung in 0 umgewandelt werden.

Die Eigenschaft " **\_ netwenum** " ist in der IDL-Definition (Interface Definition Language) für die Sammlungs Schnittstellen als eingeschränkt gekennzeichnet.

Verwenden Sie in C++ eine- `For...` Schleife, um eine Auflistung zu durchlaufen, indem Sie zuerst die Länge der Auflistung abrufen. Im folgenden Beispiel wird gezeigt, wie die Striche eines [**InkDisp**](inkdisp-class.md) -Objekts durchlaufen werden `pInk` .


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a>Parameter

Wenn Sie VT \_ Empty oder VT \_ null als Index an eine der Auflistungs Objekte in der com-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argument Werte bei der Erstellung in 0 umgewandelt werden.

## <a name="using-idispatch"></a>Verwenden von IDispatch

Um die Leistung zu verbessern, unterstützt die Tablet PC Platform com Application Programming Interface (API) das Aufrufen `IDispatchImpl::Invoke` von mit einer DISPPARAMS-Struktur mit benannten Argumenten nicht. `IDispatchImpl::GetIDsOfNames`Wird auch nicht unterstützt. Verwenden Sie stattdessen `Invoke` mit den in den SDK-Headern angegebenen DispIds.

## <a name="waiting-for-events"></a>Warten auf Ereignisse

Die Tablet PC-Umgebung ist multithreaded. Weitere Informationen finden Sie in der com-Dokumentation zum Multithreading.

## <a name="support-for-aggregation"></a>Unterstützung für Aggregation

Die Aggregation wurde nur für das [InkEdit](inkedit-control-reference.md) -Steuerelement, das [InkPicture](inkpicture-control-reference.md) -Steuerelement, das [**InkDisp**](inkdisp-class.md) -Objekt und das [**InkOverlay**](inkoverlay-class.md) -Objekt getestet. Die Aggregation wurde nicht für andere Steuerelemente und Objekte in der Bibliothek getestet.

## <a name="c"></a>C++

Die Verwendung des Tablet PC SDK in C++ erfordert die Verwendung einiger com-Konzepte wie Variant, SAFEARRAY und BSTR. In diesem Abschnitt wird beschrieben, wie Sie verwendet werden.

### <a name="variant-and-safearray"></a>Variant und SAFEARRAY

Die VARIANT-Struktur wird für die Kommunikation zwischen COM-Objekten verwendet. Im Wesentlichen handelt es sich bei der VARIANT-Struktur um einen Container für eine große Union, die viele Datentypen enthält.

Der Wert im ersten Element der Struktur, VT, beschreibt, welche der Union-Member gültig ist. Wenn Sie Informationen in einer VARIANT-Struktur erhalten, überprüfen Sie das VT-Element, um herauszufinden, welches Mitglied gültige Daten enthält. Wenn Sie Informationen mithilfe einer VARIANT-Struktur senden, legen Sie auf ähnliche Weise fest, dass VT das Unionmember enthält, das die Informationen enthält.

Bevor Sie die-Struktur verwenden, initialisieren Sie Sie, indem Sie die VariantInit com-Funktion aufrufen. Wenn die Struktur fertig ist, löschen Sie Sie, bevor der Speicher, der die Variante enthält, durch Aufrufen von VariantClear freigegeben wird.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Variant-und VARIANTARG-Datentypen](/windows/win32/api/oaidl/ns-oaidl-variant).

Die SAFEARRAY-Struktur wird als Möglichkeit bereitgestellt, mit Arrays in com sicher zu arbeiten. Das anvariant-Feld ist ein Zeiger auf ein SAFEARRAY. Verwenden Sie Funktionen wie z. b. safearraykreatevector, safearrayaccessdata und safearrayunaccessdata, um ein SAFEARRAY in einer Variante zu erstellen und auszufüllen.

Weitere Informationen zum SAFEARRAY-Datentyp finden Sie unter [SAFEARRAY-Datentyp](/windows/win32/api/oaidl/ns-oaidl-safearray).

In diesem C++-Beispiel wird ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) - `pInkStrokeDisp` Objekt in einem [**InkDisp**](inkdisp-class.md) -Objekt `pInk` aus einem Array von Punktdaten erstellt.


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a>BSTR

Das unterstützte Zeichen folgen Format für com ist BSTR. Ein BSTR weist einen Zeiger auf eine NULL-terminierte Zeichenfolge auf, enthält jedoch auch die Länge der Zeichenfolge (in Bytes, die das Abschluss Zeichen nicht zählt), die in den 4 Bytes unmittelbar vor dem ersten Zeichen der Zeichenfolge gespeichert wird.

Weitere Informationen zu BSTR finden Sie unter [BSTR-Datentyp](/previous-versions/windows/desktop/automat/bstr).

In diesem C++-Beispiel wird gezeigt, wie die Faktoid für einen [**inkrecognizercontext**](inkrecognizercontext-class.md) mithilfe eines BSTR festgelegt wird.


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
