---
description: Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344588"
---
# <a name="mf_bytestream_duration-attribute"></a>MF- \_ Bytestream- \_ Duration-Attribut

Gibt die Dauer eines Bytestreams in 100-Nanosecond-Einheiten an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Wenn das Objekt, das den Bytestream erstellt, die Dauer bestimmen kann, kann dieses Attribut festgelegt werden. (In einem Netzwerkstream kann die Dauer z. b. Teil der Sitzungs Beschreibung sein.)

Zum Abrufen des Attribut Werts können Sie **QueryInterface** für den Bytestream abrufen, um einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle zu erhalten.

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Byte Datenstrom Attribute](byte-stream-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




