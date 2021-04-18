---
description: Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354571"
---
# <a name="mft_output_types_attributes-attribute"></a>Attribut Attribute für MFT- \_ Ausgabe \_ Typen \_

Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**MFT \_ Registrieren \_ von \_ \[ \]** **als \[ Byte \]** gespeicherten Typinformationen

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.

Dieses Attribut enthält ein Array von [**MFT \_ Register \_ Type \_ Info**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) -Strukturen, die ein oder mehrere Ausgabeformate beschreiben, die vom MFT unterstützt werden. Diese Werte werden aus der Registrierung entnommen und dienen als Hinweis für die Anwendung. Die MFT unterstützt möglicherweise weitere Formate. Um das tatsächliche Ausgabeformat festzulegen, müssen Sie die MFT erstellen und [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




