---
description: Die Get-Methode ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Ikspropertyset:: Get-Methode (ksproxy. h)'
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
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481763"
---
# <a name="ikspropertysetget-method"></a>Ikspropertyset:: Get-Methode

Die **Get** -Methode ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.

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

*guidpropset* \[ in\]
</dt> <dd>

Die GUID des Eigenschaften Satzes.

</dd> <dt>

*dwpropid* \[ in\]
</dt> <dd>

Der Bezeichner der Eigenschaft innerhalb des Eigenschaften Satzes.

</dd> <dt>

*pinstancedata* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das Instanzdaten für die Eigenschaft enthält.

</dd> <dt>

*cbinstancedata* \[ in\]
</dt> <dd>

Die Größe des in *pinstancedata* angegebenen Arrays in Bytes.

</dd> <dt>

*ppropdata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Eigenschaften Daten empfängt.

</dd> <dt>

*cbpropdata* \[ in\]
</dt> <dd>

Die Größe des in *ppropdata* angegebenen Arrays in Bytes.

</dd> <dt>

*pcbreturned* \[ vorgenommen\]
</dt> <dd>

Empfängt die Anzahl von Bytes, die von der Methode in das *ppropdata* -Array kopiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                                                         |
| <dl> <dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt> </dl> | Der Eigenschaften Satz wird nicht unterstützt.<br/>                               |
| <dl> <dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt> </dl>  | Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte " [ikscontrol](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Um eine Eigenschaft abzurufen, weisen Sie einen Puffer zu, der von dieser Methode ausgefüllt wird. Um die erforderliche Puffergröße zu ermitteln, **Geben Sie** für " *ppropdata* " den Wert NULL und für *cbpropdata* den Wert 0 (null) an. Diese Methode gibt die erforderliche Puffergröße in *pcbreturned* zurück.

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine PIN für die PIN-Kategorie durch Abrufen der Eigenschaft **amproperty- \_ Pin- \_ Kategorie** abgefragt. (Siehe [PIN-Eigenschaften Satz](pin-property-set.md).)


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
| Header<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**"Ikspropertyset"-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 
