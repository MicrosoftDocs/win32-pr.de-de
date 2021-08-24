---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für die Initialisierung verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8126bfea15f9946bb9950293a6c39c101f9c37c8870176fb4bb0108aa5862bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723460"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH-Eigenschaft

Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für die Initialisierung verwenden kann.


## <a name="data-type"></a>Datentyp

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>Eigenschaften-GUID

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Eigenschaftswert

Ein Dateipfad, der einen Speicherort darstellt, den das Content Decryption Module (CDM) für die Initialisierung verwenden kann.

## <a name="remarks"></a>Hinweise

Der mit dieser Eigenschaft angegebene Pfad wird auch für inhaltsspezifische Daten verwendet, wenn die [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH-Eigenschaft](mf-contentdecryptionmodule-inprivatestorepath.md) nicht festgelegt ist.

Um die COM-Leistung zu verbessern, sollte die App den Speicherort nicht löschen, nachdem das CDM-Objekt freigegeben wurde.



Legen Sie diese Eigenschaft fest, wenn Sie eine CDM-Datei erstellen, indem [Sie DURCH AUFRUFEN VON DENKContentDecryptionModuleAccess::CreateContentDecryptionModule aufrufen.](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020 Update<br/>                                     |
| Header<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

- [Media Foundation Eigenschaften](media-foundation-properties.md)
- [CODContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




