---
description: Die KsQueryMediums-Methode ruft die von einem Pin unterstützten Medien ab.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: IKsPin::KsQueryMediums-Methode (Ksproxy.h)
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
ms.openlocfilehash: 33edb7cb2ca959080878f7ce735930ceec9d95dc2f829aef6d50f72d764f2f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398936"
---
# <a name="ikspinksquerymediums-method"></a>IKsPin::KsQueryMediums-Methode

Die `KsQueryMediums` -Methode ruft die von einem Pin unterstützten Medien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppmi* \[ out\]
</dt> <dd>

Adresse eines Zeigers auf eine [**KSMULTIPLE \_ ITEM-Struktur.**](ksmultiple-item.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode gibt eine aufgabenbasierte [**KSMULTIPLE \_ ITEM-Struktur**](ksmultiple-item.md) zurück, auf die 0 (null) oder mehr [**REGPINMEDIUM-Strukturen**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) folgen. Das **Count-Element** der **KSMULTIPLE \_ ITEM-Struktur** gibt die Anzahl der **REGPINMEDIUM-Strukturen** an. Jede **REGPINMEDIUM-Struktur** definiert ein Medium, das vom Pin unterstützt wird.

Der Aufrufer muss die zurückgegebenen Strukturen mithilfe der **CoTaskMemFree-Funktion** frei geben.

Sie müssen Ks.h vor Ksproxy.h angeben.

## <a name="examples"></a>Beispiele

Die folgende Hilfsfunktion versucht, eine Stecknadel mit einem angegebenen Medium zu ab stimmen.


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
| Header<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IKsPin-Schnittstelle**](ikspin.md)
</dt> <dt>

[WDM-Klassentreiberfilter](wdm-class-driver-filters.md)
</dt> </dl>

 

 




