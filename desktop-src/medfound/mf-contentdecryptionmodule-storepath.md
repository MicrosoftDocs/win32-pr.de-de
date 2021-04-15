---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Inhalts Entschlüsselungsmodul (CDM) für die Initialisierung verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485219"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>StorePath-Eigenschaft des MF- \_ contentdecryptionmodule \_

Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Inhalts Entschlüsselungsmodul (CDM) für die Initialisierung verwenden kann.


## <a name="data-type"></a>Datentyp

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>Eigenschaften-GUID

**der MF- \_ contentdecryptionmodule \_ StorePath**

## <a name="property-value"></a>Eigenschaftswert

Ein Dateipfad, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für die Initialisierung verwenden kann.

## <a name="remarks"></a>Bemerkungen

Der mit dieser Eigenschaft angegebene Pfad wird auch für inhaltsspezifische Daten verwendet, wenn die [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) -Eigenschaft nicht festgelegt ist.

Um die com-Leistung zu verbessern, sollte die APP den Speicherort nicht löschen, nachdem das CDM-Objekt freigegeben wurde.



Legen Sie diese Eigenschaft fest, wenn Sie einen CDM durch Aufrufen von [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020-Update<br/>                                     |
| Header<br/>                   | <dl> <dt>MF contentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

- [Eigenschaften von Media Foundation](media-foundation-properties.md)
- [Imbcontentdecryptionmoduleaccess:: kreatecontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




