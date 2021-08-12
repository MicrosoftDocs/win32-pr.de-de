---
description: Die Get-Methode ruft eine Eigenschaft ab, die durch eine Eigenschaftensatz-GUID und eine Eigenschaften-ID identifiziert wird.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: IKsPropertySet::Get-Methode (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652242"
---
# <a name="ikspropertysetget-method"></a>IKsPropertySet::Get-Methode

Die **Get-Methode** ruft eine Eigenschaft ab, die durch eine Eigenschaftensatz-GUID und eine Eigenschaften-ID identifiziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidPropSet* \[ In\]
</dt> <dd>

Die GUID des Eigenschaftensets.

</dd> <dt>

*dwPropID* \[ In\]
</dt> <dd>

Der Bezeichner der Eigenschaft innerhalb des Eigenschaftensets.

</dd> <dt>

*pInstanceData* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das Instanzdaten für die -Eigenschaft enthält.

</dd> <dt>

*cbInstanceData* \[ In\]
</dt> <dd>

Die Größe des in *pInstanceData* angegebenen Arrays in Bytes.

</dd> <dt>

*pPropData* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Eigenschaftsdaten empfängt.

</dd> <dt>

*cbPropData* \[ In\]
</dt> <dd>

Die Größe des in *pPropData* angegebenen Arrays in Bytes.

</dd> <dt>

*– Wiederernent* \[ out\]
</dt> <dd>

Empfängt die Anzahl der Bytes, die die Methode in das *pPropData-Array* kopiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                                                         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | Der Eigenschaftensatz wird nicht unterstützt.<br/>                               |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | Die Eigenschaften-ID wird für den angegebenen Eigenschaftensatz nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Headerdatei dsound.h vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die [IKsControl-Schnittstelle,](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) die im DirectShow-DDK dokumentiert ist, ist jetzt die empfohlene Schnittstelle zum Übergeben von Eigenschaftensätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Ordnen Sie zum Abrufen einer Eigenschaft einen Puffer zu, den diese Methode dann ausfüllt. Um die erforderliche Puffergröße zu bestimmen, geben Sie **NULL** für *pPropData und* null (0) für *cbPropData an.* Diese Methode gibt die erforderliche Puffergröße in *"wirreturned" zurück.*

Sie müssen Ks.h vor Ksproxy.h angeben.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Stecknadel für die Pinkategorie abgefragt, indem die **AMPROPERTY \_ PIN \_ CATEGORY-Eigenschaft abgerufen** wird. (Siehe [Pin-Eigenschaftssatz](pin-property-set.md).)


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
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

[**IKsPropertySet-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 
