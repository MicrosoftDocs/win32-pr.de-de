---
description: Die inondelegatingunknown-Schnittstelle ist eine Version von IUnknown, die umbenannt wird, um die Unterstützung für die nicht Delegierung und Delegierung von IUnknown-Schnittstellen im selben com-Objekt zu ermöglichen.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: Inondelegatingunknown (ComBase. h)
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
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370288"
---
# <a name="inondelegatingunknown"></a>Inondelegatingunknown

Die- `INonDelegatingUnknown` Schnittstelle ist eine Version von **IUnknown** , die umbenannt wird, um die Unterstützung für die nicht Delegierung und Delegierung von **IUnknown** -Schnittstellen im gleichen com-Objekt zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Bemerkungen

Führen Sie `INonDelegatingUnknown` die folgenden Schritte aus, um für die mehrfache Vererbung zu verwenden.

1.  Leiten Sie die Klasse von einer Schnittstelle ab, z. b. IMyInterface.
2.  Fügen [**Sie \_ Declare IUnknown**](declare-iunknown.md) in die Klassendefinition ein, um Implementierungen von **QueryInterface**, **adressf** und **Release** zu deklarieren, die das äußere unbekannte-Element aufzurufen.
3.  Überschreiben Sie **nondelegatingqueryinterface** , um IMyInterface mit Code wie dem folgenden verfügbar zu machen:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Deklarieren und implementieren Sie die Element Funktionen von IMyInterface.

Führen Sie `INonDelegatingUnknown` die folgenden Schritte aus, um für die-Schnittstellen zu verwenden:

1.  Deklarieren Sie eine von [**cunknown**](cunknown.md)abgeleitete Klasse.
2.  Include [**Declare \_ IUnknown**](declare-iunknown.md) in der Klassendefinition.
3.  Überschreiben Sie **nondelegatingqueryinterface** , um IMyInterface mit dem folgenden Code verfügbar zu machen:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implementieren Sie die Member-Funktionen von IMyInterface. Verwenden Sie [**cunknown:: GetOwner**](cunknown-getowner.md) , um auf die com-Objektklasse zuzugreifen.
5.  Legen Sie in der com-Objektklasse die-Klasse als Friend der com-Objektklasse ab, und deklarieren Sie eine Instanz der-Klasse als Member der com-Objektklasse.

Da Sie den äußeren unbekannten und ein **HRESULT** immer an den [**cunknown**](cunknown.md) -Konstruktor übergeben müssen, können Sie keinen Standardkonstruktor verwenden. Sie müssen die Member-Variable zu einem Zeiger auf die Klasse machen und einen neuen-Befehl in Ihrem Konstruktor erstellen, um Sie tatsächlich zu erstellen.

Überschreiben Sie die **nondelegatingqueryinterface** mit folgendem Code:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Sie können gemischte Klassen haben, die einige Schnittstellen durch mehrfache Vererbung und einige Schnittstellen durch schsted Klassen unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> </dl>

 

 




