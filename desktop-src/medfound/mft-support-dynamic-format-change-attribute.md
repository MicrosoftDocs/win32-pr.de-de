---
description: Gibt an, ob eine Media Foundation Transformation (MFT) dynamische Formatänderungen unterstützt.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354621"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>MFT- \_ Unterstützung des \_ dynamischen \_ Format \_ Änderungs Attributs

Gibt an, ob eine Media Foundation Transformation (MFT) dynamische Formatänderungen unterstützt.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann die folgenden Werte aufweisen.



| Wert     | BESCHREIBUNG                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Der Client kann beim Streaming das Eingabeformat ändern.               |
| **FALSE** | Der MFT muss entladen werden, bevor der Client das Eingabeformat ändern kann. |



 

Zum Abrufen dieses Attributs müssen Sie zuerst [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher für die MFT zu erhalten. Anschließend können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) abrufen, um den Attribut Wert zu erhalten.

Wenn [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fehlschlägt oder das-Attribut nicht vorhanden ist, ist der Standardwert **false**.

[Asynchrone MFTs](asynchronous-mfts.md) müssen den Wert " **true**" zurückgeben.

Weitere Informationen finden Sie unter [Handling Stream Changes](handling-stream-changes.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




