---
description: Gibt die maximale Anzahl von Ausgabe Beispielen an, die eine Microsoft Media Foundation Transformation (MFT) jederzeit in der Pipeline aussteht.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214884"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>VM \_ - \_ \_ mindestausgabe \_ Sample \_ count-Attribut

Gibt die maximale Anzahl von Ausgabe Beispielen an, die eine Microsoft Media Foundation Transformation (MFT) jederzeit in der Pipeline aussteht.

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
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




