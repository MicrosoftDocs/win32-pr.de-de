---
description: Die INonDelegatingUnknown-Schnittstelle ist eine Version von IUnknown, die umbenannt wird, um unterstützung für nicht delegierende und delegierende IUnknown-Schnittstellen im gleichen COM-Objekt zu ermöglichen.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f733ba28af1b4ecb7fc0a52852b4d8663fddf1df07572c409136a9aa963ba076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051610"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

Die `INonDelegatingUnknown` Schnittstelle ist eine Version von **IUnknown,** die umbenannt wird, um unterstützung für nicht delegierende und delegierende **IUnknown-Schnittstellen** im gleichen COM-Objekt zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Hinweise

Führen `INonDelegatingUnknown` Sie die folgenden Schritte aus, um für mehrfache Vererbung zu verwenden.

1.  Leiten Sie Ihre Klasse von einer Schnittstelle ab, z. B. IMyInterface.
2.  Schließen Sie [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) in Ihre Klassendefinition ein, um Implementierungen von **QueryInterface,** **AddRef** und **Release** zu deklarieren, die das äußere Unbekannte aufrufen.
3.  Überschreiben Sie **NonDelegatingQueryInterface,** um IMyInterface mit Code wie dem folgenden verfügbar zu machen:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Deklarieren und implementieren Sie die Memberfunktionen von IMyInterface.

Führen `INonDelegatingUnknown` Sie die folgenden Schritte aus, um für geschachtelte Schnittstellen zu verwenden:

1.  Deklarieren Sie eine von [**CUnknown**](cunknown.md)abgeleitete Klasse.
2.  Schließen Sie [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) in Ihre Klassendefinition ein.
3.  Überschreiben Sie **NonDelegatingQueryInterface,** um IMyInterface mit dem Folgenden verfügbar zu machen:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implementieren Sie die Memberfunktionen von IMyInterface. Verwenden Sie [**CUnknown::GetOwner,**](cunknown-getowner.md) um auf die COM-Objektklasse zuzugreifen.
5.  Machen Sie die geschachtelte Klasse in ihrer COM-Objektklasse zu einem Friend der COM-Objektklasse, und deklarieren Sie eine Instanz der geschachtelten Klasse als Member der COM-Objektklasse.

Da Sie immer das äußere Unbekannte und ein **HRESULT** an den [**CUnknown-Konstruktor**](cunknown.md) übergeben müssen, können Sie keinen Standardkonstruktor verwenden. Sie müssen die Membervariable zu einem Zeiger auf die Klasse machen und einen neuen Aufruf in Ihrem Konstruktor vornehmen, um sie tatsächlich zu erstellen.

Überschreiben Sie **NonDelegatingQueryInterface** mit Code wie dem folgenden:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Sie können gemischte Klassen verwenden, die einige Schnittstellen durch mehrere Vererbung unterstützen, und einige Schnittstellen über geschachtelte Klassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> </dl>

 

 




