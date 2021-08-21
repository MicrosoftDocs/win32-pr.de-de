---
description: Ruft Statistiken aus der MEDIENSenke der Digital Living Network Alliance (DLNA) ab.
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS -Attribut (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a80bf0682cf6e46845a968122bf512a6e9cff15df8fb8e0312e1c63c8dab0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973619"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>MF \_ MP2DLNA \_ STATISTICS-Attribut

Ruft Statistiken aus der MEDIENSenke der Digital Living Network Alliance (DLNA) ab.

## <a name="data-type"></a>Datentyp

**[**MFMPEG2DLNASINKSTATS als**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** **BYTE gespeichert \[ \]**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

## <a name="remarks"></a>Hinweise

Während des Streamings aktualisiert die DLNA-Mediensenke dieses Attribut mit Statistiken zur Codierung und zum Multiplexing der MPEG-2-Streams. Die Anwendung kann dieses Attribut jederzeit abfragen, um die neuesten Werte zu erhalten.

Das Festlegen dieses Attributs auf die DLNA-Mediensenke hat keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




