---
description: Ruft Statistiken aus der Datenträger-Senke der digitalen Lebens Netzwerk-Allianz (DLNA) ab.
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528256"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>MF \_ MP2DLNA \_ Statistics-Attribut

Ruft Statistiken aus der Datenträger-Senke der digitalen Lebens Netzwerk-Allianz (DLNA) ab.

## <a name="data-type"></a>Datentyp

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** als **Byte \[ \]** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

## <a name="remarks"></a>Bemerkungen

Während des Streamings aktualisiert die DLNA-Medien Senke dieses Attribut mit Statistiken über die Codierung und das Multiplexing der MPEG-2-Streams. Die Anwendung kann dieses Attribut jederzeit Abfragen, um die aktuellen Werte zu erhalten.

Das Festlegen dieses Attributs für die DLNA-Medien Senke hat keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




