---
description: Die ksquerymediums-Methode ruft die von einer PIN unterstützten Medien ab.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Ikspin:: ksquerymediums-Methode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746576"
---
# <a name="ikspinksquerymediums-method"></a>Ikspin:: ksquerymediums-Methode

Die- `KsQueryMediums` Methode ruft die von einer PIN unterstützten Medien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmi* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers auf eine [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt eine Aufgabe zugeordnete [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur zurück, auf die 0 (null) oder mehr [**regpinmedium**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) -Strukturen folgt. Der **count** -Member der **ksmultiple- \_ Element** Struktur gibt die Anzahl der **regpinmedium** -Strukturen an. Jede **regpinmedium** -Struktur definiert ein Medium, das von der PIN unterstützt wird.

Der Aufrufer muss die zurückgegebenen Strukturen mit der **CoTaskMemFree** -Funktion freigeben.

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="examples"></a>Beispiele

Die folgende Hilfsfunktion versucht, eine PIN mit einem angegebenen Medium abzugleichen.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**Ikspin-Schnittstelle**](ikspin.md)
</dt> <dt>

[WDM-Klassen Treiber Filter](wdm-class-driver-filters.md)
</dt> </dl>

 

 




