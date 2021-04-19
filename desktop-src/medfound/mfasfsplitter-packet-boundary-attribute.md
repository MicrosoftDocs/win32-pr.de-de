---
description: Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält.
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348828"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>Mfasarsplitter- \_ Paket \_ Begrenzungs Attribut

Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Wenn ein Medien Puffer die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle über **QueryInterface** verfügbar macht und der Wert dieses Attributs ungleich NULL ist, behandelt der ASF-Splitter den Puffer als Anfang eines neuen Pakets.

Dieses Attribut gilt, wenn Sie den ASF-Splitter zum Analysieren von ASF-Daten verwenden. Wenn Ihre ASF-Daten über Variable Paket Längen verfügen, müssen Sie dieses Attribut für die Medien Puffer festlegen, die Sie an die [**imfasfsplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) -Methode übergeben. Legen Sie das-Attribut auf **true** fest, wenn der Puffer den Anfang eines neuen Pakets enthält. Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das-Attribut auf " **false**" fest. Die Puffer können nicht mehrere Pakete umfassen.

Bei ASF-Daten mit fester Paketgröße ist dieses Attribut nicht erforderlich, und ein Puffer kann mehrere Pakete umfassen.

Beachten Sie, dass die Standard Implementierungen von [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , die von Media Foundation bereitgestellt werden, keine [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)verfügbar machen. Um dieses Attribut zu verwenden, müssen Sie eine eigene Implementierung von **imfmediabuffer** bereitstellen. beispielsweise durch das umwickeln der von [**MF | atememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer)zurückgegebenen Puffer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Attribute](asf-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




