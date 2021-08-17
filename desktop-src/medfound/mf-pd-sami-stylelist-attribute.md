---
description: Enthält die Anzeigenamen der SAMI-Stile (Synchronized Accessible Media Interchange), die in der SAMI-Datei definiert sind.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f57d418eb86c19d3aa2db12808dde810456c38ec6abd45fbece450b30f60f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876173"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>MF \_ PD \_ SAMI \_ STYLELIST-Attribut

Enthält die Anzeigenamen der SAMI-Stile (Synchronized Accessible Media Interchange), die in der SAMI-Datei definiert sind.

Die [SAMI-Medienquelle](sami-media-source.md) legt dieses Attribut für den von ihm erstellten Präsentationsdeskriptor fest.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Das Attributblob weist die folgende Struktur auf:



Datentyp

Beschreibung

Größe (Byte)

**DWORD**

Anzahl der Formatzeichenfolgen.

4

Für jede Formatzeichenfolge:

**DWORD**

Größe der Zeichenfolge in Bytes, einschließlich des **NULL-Zeichens.**

4

**Lpwstr**

Auf NULL endende Breitzeichenzeichenfolge, die den Namen des Stils enthält.

Varies



 

Verwenden Sie zum Festlegen des Stils oder Abrufen des aktuellen Stils die [**SCHNITTSTELLE "STYLESSAMIStyle".**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="examples"></a>Beispiele


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[SAMI-Medienquelle](sami-media-source.md)
</dt> </dl>

 

 




