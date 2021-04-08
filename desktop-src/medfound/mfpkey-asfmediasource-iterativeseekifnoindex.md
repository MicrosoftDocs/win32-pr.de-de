---
description: Konfiguriert die ASF-Medienquelle für die Verwendung von iterativer Suche, wenn die Quelldatei über keinen Index verfügt.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761448"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>Mfpkey \_ asfmediasource \_ iterativeseekifnoindex (Eigenschaft)

Konfiguriert die ASF-Medienquelle für die Verwendung von iterativer Suche, wenn die Quelldatei über keinen Index verfügt.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den *quellresolver*. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

*Iteratives suchen* ist ein Algorithmus, mit dem eine Position in einer ASF-Datei ohne Index gefunden wird. Es verwendet eine Reihe von Näherungen, die auf der durchschnittlichen Bitrate basieren, um die Ziel Suchzeit progressiv näher zu bringen. (Der Algorithmus ähnelt einer binären Suche.) Das iterative suchen kann länger dauern als die Suche nach Index, daher ist es standardmäßig deaktiviert.

Wenn Sie diese Eigenschaft festlegen, verwenden Sie die folgenden Eigenschaften, um die Suchparameter festzulegen:

-   [Mfpkey \_ asfmediasource \_ iterativeseek \_ Maximale \_ Anzahl](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [Mfpkey \_ asfmediasource \_ iterativeseek \_ Tolerance \_ in \_ Millisekunde](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Diese Eigenschaften legen die maximale Anzahl von Iterationen bzw. die Toleranz fest. Der Algorithmus wird angehalten, wenn die maximale Anzahl von Iterationen erreicht wird, oder wenn ein Paket gefunden wird, dessen Entfernung von der Suchzeit innerhalb der angegebenen Toleranz liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




