---
description: Übersicht über die COM-Bibliothek und Hinweise zur Verwendung der Tablet PC-Technologieabschnitte des Windows Vista SDK.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Verwenden der COM-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819140"
---
# <a name="using-the-com-library"></a>Verwenden der COM-Bibliothek

Die Referenz zur verwalteten Tablet PC-Bibliothek finden Sie jetzt im regulären Abschnitt referenz Windows Vista SDK Class Library . Sie stellt ein Objektmodell für Microsoft Visual C++ bereit. Die meisten Objekte in der COM-Bibliothek sind identisch mit denen in der verwalteten API für Tablet-PCs.

Die COM-API enthält jedoch zusätzlich zu den Membern, die in der verwalteten API gefunden werden, aufgrund der Unterschiede zwischen der Standardmäßige Microsoft Win32-Umgebung und der Microsoft .NET FrameworkSoftware Development Kit (SDK)-Umgebung. Beispielsweise werden die Objekte InkRectangle und InkTransform in COM verwendet, aber das FrameworkSDK bietet eine native Implementierung für [**die InkRectangle-Klasse**](inkrectangle-class.md) und [**die InkTransform-Klasse,**](inktransform-class.md) die die Notwendigkeit dieser Objekte in der verwalteten API der Tablet PC-Plattform entfällt.

> [!Note]  
> Die Objekte in der COM-API und die Ink-Steuerelemente sind nicht für die Verwendung in Active Server Pages (ASP) konzipiert.

 

## <a name="working-with-collections"></a>Arbeiten mit Sammlungen

Wenn Sie einen **NULL-Wert** als Index an eines der Auflistungsobjekte in der COM-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argumentwerte beim Aufruf auf 0 (null) gesetzt werden.

Die **\_ NewEnum-Eigenschaft** ist in der Definition der Schnittstellendefinitionssprache (Interface Definition Language, IDL) für die Auflistungsschnittstellen als eingeschränkt gekennzeichnet.

Verwenden Sie in C++ eine `For...` -Schleife, um eine Auflistung zu durchlaufen, indem Sie zuerst die Länge der Sammlung abrufen. Das folgende Beispiel zeigt, wie die Striche eines [**InkDisp-Objekts**](inkdisp-class.md) durchlaufen werden. `pInk`


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

Wenn Sie VT \_ EMPTY oder VT NULL als Index an eines \_ der Auflistungsobjekte in der COM-Bibliothek übergeben, erhalten Sie das erste Element in der Auflistung, da diese Argumentwerte beim Aufruf auf 0 (null) gesetzt werden.

## <a name="using-idispatch"></a>Verwenden von IDispatch

Um die Leistung zu steigern, unterstützt die COM-Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) von Tablet PC Platform keine Aufrufe `IDispatchImpl::Invoke` mit einer DISPPARAMS-Struktur mit benannten Argumenten. `IDispatchImpl::GetIDsOfNames`Wird auch nicht unterstützt. Rufen Sie stattdessen `Invoke` mit den in den SDK-Headern angegebenen DISPIDs auf.

## <a name="waiting-for-events"></a>Warten auf Ereignisse

Die Tablet PC-Umgebung ist multithreaded. Informationen zum Multithreading finden Sie in der COM-Dokumentation.

## <a name="support-for-aggregation"></a>Unterstützung für Aggregation

Aggregation wurde nur für das [InkEdit-Steuerelement,](inkedit-control-reference.md) das [InkPicture-Steuerelement,](inkpicture-control-reference.md) das [**InkDisp-Objekt**](inkdisp-class.md) und das [**InkOverlay-Objekt**](inkoverlay-class.md) getestet. Die Aggregation wurde nicht für andere Steuerelemente und Objekte in der Bibliothek getestet.

## <a name="c"></a>C++

Die Verwendung des Tablet PC SDK in C++ erfordert die Verwendung einiger COM-Konzepte wie VARIANT, SAFEARRAY und BSTR. In diesem Abschnitt wird beschrieben, wie sie verwendet werden.

### <a name="variant-and-safearray"></a>VARIANT und SAFEARRAY

Die VARIANT-Struktur wird für die Kommunikation zwischen COM-Objekten verwendet. Im Wesentlichen ist die VARIANT-Struktur ein Container für eine große Union, die viele Arten von Daten enthält.

Der Wert im ersten Member der -Struktur, vt, beschreibt, welche der Union-Member gültig sind. Wenn Sie Informationen in einer VARIANT-Struktur erhalten, überprüfen Sie den vt-Member, um herauszufinden, welcher Member gültige Daten enthält. Wenn Sie Informationen mithilfe einer VARIANT-Struktur senden, legen Sie vt entsprechend dem Union-Member fest, der die Informationen enthält.

Bevor Sie die -Struktur verwenden, initialisieren Sie sie, indem Sie die VariantInit-COM-Funktion aufrufen. Wenn Sie mit der -Struktur fertig sind, löschen Sie sie, bevor der Arbeitsspeicher, der die VARIANT enthält, durch Aufrufen von VariantClear freigegeben wird.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [VARIANT- und VARIANTARG-Datentypen.](/windows/win32/api/oaidl/ns-oaidl-variant)

Die SAFEARRAY-Struktur wird als Möglichkeit zum sicheren Arbeiten mit Arrays in COM bereitgestellt. Das Parrayfeld von VARIANT ist ein Zeiger auf ein SAFEARRAY. Verwenden Sie Funktionen wie SafeArrayCreateVector, SafeArrayAccessData und SafeArrayUnaccessData, um ein SAFEARRAY in einer VARIANT-Datei zu erstellen und zu füllen.

Weitere Informationen zum SAFEARRAY-Datentyp finden Sie unter [SafeArray-Datentyp.](/windows/win32/api/oaidl/ns-oaidl-safearray)

In diesem C++-Beispiel wird ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ,-Objekt `pInkStrokeDisp` in einem [**InkDisp-Objekt**](inkdisp-class.md) `pInk` aus einem Array von Punktdaten erstellt.


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

Das unterstützte Zeichenfolgenformat für COM ist BSTR. Ein BSTR verfügt über einen Zeiger auf eine auf null endende Zeichenfolge, enthält aber auch die Länge der Zeichenfolge (in Bytes, ohne Zählung des Abschlusszeichens), die in den 4 Bytes unmittelbar vor dem ersten Zeichen der Zeichenfolge gespeichert wird.

Weitere Informationen zu BSTR finden Sie unter [BSTR-Datentyp.](/previous-versions/windows/desktop/automat/bstr)

In diesem C++-Beispiel wird gezeigt, wie sie das Factoid mithilfe eines BSTR für [**einen InkRecognizerContext**](inkrecognizercontext-class.md) festlegen.


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



 

 
