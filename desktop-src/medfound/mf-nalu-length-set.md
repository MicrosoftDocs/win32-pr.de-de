---
description: Gibt an, dass NALU-Längeninformationen als BLOB mit jedem komprimierten H.264-Beispiel gesendet werden.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104386"
---
# <a name="mf_nalu_length_set-attribute"></a>MF \_ NALU \_ LENGTH \_ SET-Attribut

Gibt an, dass NALU-Längeninformationen als **BLOB** mit jedem komprimierten H.264-Beispiel gesendet werden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Legen Sie dieses Attribut auf den Eingabemedientyp MEDIASUBTYPE \_ H264 fest.

Legen Sie MF \_ NALU \_ LENGTH SET für \_ den Eingabemedientyp H.264-Decoder fest, um anzugeben, dass für jedes Eingabebeispiel eine NALU-Länge verfügbar ist und jedes Eingabebeispiel ein vollständiges primäres Bild enthält.

Das **BLOB,** das die NALU-Längeninformationen enthält, kann aus dem [MF \_ NALU LENGTH \_ \_ INFORMATION-Attribut](mf-nalu-length-information.md) im Eingabebeispiel abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




