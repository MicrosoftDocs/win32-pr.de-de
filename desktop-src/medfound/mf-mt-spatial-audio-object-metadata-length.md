---
description: Ein-Wert, der die Größe des Datentyps für räumliche audiometadaten angibt, der vom Decoder ausgegeben wird.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216271"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>MF \_ \_ \_ - \_ Objekt \_ metadatenlängen-Attribut für räumliche Audioobjekte \_

Ein-Wert, der die Größe des Datentyps für räumliche audiometadaten angibt, der vom Decoder ausgegeben wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Das metadatenblob mit dem angegebenen Format wird mithilfe der [**ispatialaudiometadatawriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) -Schnittstelle geschrieben und mithilfe der [**ispatialaudiometadatareader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) -Schnittstelle gelesen. Das metadatenblob ist für die Media Foundation Pipeline und die Komponenten nicht transparent. Das-Attribut wird auf den Typ des räumlichen audiomediums angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
