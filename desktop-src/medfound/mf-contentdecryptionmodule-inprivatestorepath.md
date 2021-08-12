---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für inhaltsspezifische Daten verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244773"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH-Eigenschaft

Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für inhaltsspezifische Daten verwenden kann.


## <a name="data-type"></a>Datentyp

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>Eigenschaften-GUID

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Eigenschaftswert

Ein Dateipfad, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für inhaltsspezifische Daten verwenden kann.

## <a name="remarks"></a>Hinweise

Die App sollte den Speicherort löschen, nachdem das CDM-Objekt freigegeben wurde.

Wenn diese Eigenschaft nicht festgelegt ist, verwendet das System den mit der [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) -Eigenschaft angegebenen Pfad für inhaltsspezifische Daten.

Legen Sie diese Eigenschaft fest, wenn Sie ein CDM erstellen, indem Sie ["CONTENTDecryptionModuleAccess::CreateContentDecryptionModule"](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020 Update<br/>                                     |
| Header<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

- [Media Foundation-Eigenschaften](media-foundation-properties.md)
- [CONTENTDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




