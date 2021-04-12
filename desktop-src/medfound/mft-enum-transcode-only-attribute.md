---
description: Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393582"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>Attribut Attribut für MFT-Aufzählung von \_ \_ transcode \_ \_

Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.

Derzeit gilt dieses Attribut nur für hardwarebasierte decoderer, die den AVStream-Mini Treiber verwenden. Das-Attribut wird in der Registrierung unter den Funktions Informationen des Decoders gespeichert. Weitere Informationen finden Sie in der Dokumentation zu [**igetcapabilitieskey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Anwendungen verwenden dieses Attribut in der Regel nicht.

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Wenn dieser Registrierungs Eintrag vorhanden und gleich 1 ist, überspringt die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion den Decoder, es sei denn, der Aufrufer hat das Flag " **\_ \_ \_ \_ nur transcode" der MFT** -Enumeration in " **mftenumex**" angegeben.

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

[**MF-Datei**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
