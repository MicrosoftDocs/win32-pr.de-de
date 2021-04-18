---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526900"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>"MF \_ contentdecryptionmodule" \_ inprivatestorepath (Eigenschaft)

Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.


## <a name="data-type"></a>Datentyp

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>Eigenschaften-GUID

**MF \_ contentdecryptionmodule \_ inprivatestorepath**

## <a name="property-value"></a>Eigenschaftswert

Ein Dateipfad, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.

## <a name="remarks"></a>Bemerkungen

Die APP sollte den Speicherort löschen, nachdem das CDM-Objekt freigegeben wurde.

Wenn diese Eigenschaft nicht festgelegt ist, verwendet das System den Pfad, der mit der [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) -Eigenschaft für inhaltsspezifische Daten angegeben wird.

Legen Sie diese Eigenschaft fest, wenn Sie einen CDM durch Aufrufen von [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020-Update<br/>                                     |
| Header<br/>                   | <dl> <dt>MF contentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

- [Eigenschaften von Media Foundation](media-foundation-properties.md)
- [Imbcontentdecryptionmoduleaccess:: kreatecontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




