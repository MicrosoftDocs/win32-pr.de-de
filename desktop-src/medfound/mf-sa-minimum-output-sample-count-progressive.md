---
description: Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation Transform (MFT) zulassen soll, dass Sie zu einem beliebigen Zeitpunkt überstehen.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216877"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>\_ \_ \_ \_ \_ Anzahl \_ progressives Attribute der MF SA-Ausgabe Stichprobe

Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation Transform (MFT) zulassen soll, dass Sie zu einem beliebigen Zeitpunkt überstehen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt nur für MFTs, die einen Zirkel Puffer verwenden, um eigene Ausgabe Beispiele zuzuordnen. Andere MFTs ignorieren dieses Attribut.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.
2.  Zum Hinzufügen des Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




