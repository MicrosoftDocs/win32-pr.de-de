---
description: Enthält die anzeigen amen der in der Sami-Datei definierten Sami-Stile (in der Datei mit synchroner Barrierefreiheit).
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868547"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>MF \_ PD, \_ Sami \_ stylelist-Attribut

Enthält die anzeigen amen der in der Sami-Datei definierten Sami-Stile (in der Datei mit synchroner Barrierefreiheit).

Die [Sami Media-Quelle](sami-media-source.md) legt dieses Attribut auf dem Präsentations Deskriptor fest, den Sie erstellt.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Das Attribut-BLOB weist die folgende Struktur auf:



Datentyp

BESCHREIBUNG

Größe (Byte)

**DWORD**

Anzahl von Format Zeichenfolgen.

4

Für jede Format Zeichenfolge:

**DWORD**

Größe der Zeichenfolge in Bytes, einschließlich des **null** -Zeichens.

4

**LPWSTR**

Eine auf NULL endenden Zeichenfolge mit breit Zeichen, die den Namen des Stils enthält.

Varies



 

Um den Stil festzulegen oder den aktuellen Stil abzurufen, verwenden Sie die [**imfsamistyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) -Schnittstelle.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[Sami-Medienquelle](sami-media-source.md)
</dt> </dl>

 

 




