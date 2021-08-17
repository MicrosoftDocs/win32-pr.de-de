---
description: Gibt die Längen von NALUs im Beispiel an. Dies ist ein MF-BLOB, das für komprimierte Eingabebeispiele auf den H.264-Decoder festgelegt ist.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2020c0086247adda742ce2613045bb3a2004c3b8c13c7cdcb04a0ff3997cf0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104416"
---
# <a name="mf_nalu_length_information-attribute"></a>MF \_ NTRIBU \_ LENGTH \_ INFORMATION-Attribut

Gibt die Längen von NALUs im Beispiel an. Dies ist ein **MF-BLOB,** das für komprimierte Eingabebeispiele auf den H.264-Decoder festgelegt ist.

## <a name="data-type"></a>Datentyp

**Blob**

## <a name="remarks"></a>Hinweise

Damit dieses Attribut festgelegt werden kann, muss das Medium vom Typ MEDIASUBTYPE H264 sein, und das \_ [MF \_ N ENUMERATION \_ LENGTH \_ SET-Attribut](mf-nalu-length-set.md) muss für den Eingabemedientyp von MEDIASUBTYPE \_ H264 festgelegt werden.

Legen Sie MF NWORD LENGTH INFORMATION als BLOB für das Eingabebeispiel fest, mit einem \_ \_ \_ DWORD für jede NLECK im Beispiel.  Wenn beispielsweise AUD (9 Bytes), SPS (25 Byte), PPS (10 Byte), IDR-Slice1 (50 k), IDR-Slice 2 (60 k) enthalten sind, sollten fünf DWORDs mit den Werten 9, 25, 10, 50 k, 60 k im **BLOB** enthalten sein.

Hier code that sets the **BLOB**, where **rgdwNWORDLengthInfo** is an array of type DWORD and **uiN kachelLengthIdx** is the valid NWORD lengths set to the **BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




