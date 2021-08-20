---
description: Enthält einen Zeiger auf einen Eigenschaftenspeicher mit Codierungseigenschaften.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb68348987ac406643cbe709dc6052d1add3c04e63b4e1f38d7c681a95c3ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059084"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>MF \_ SINK WRITER ENCODER \_ \_ \_ CONFIG-Attribut

Enthält einen Zeiger auf einen Eigenschaftenspeicher mit Codierungseigenschaften.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein [**IPropertyStore-Zeiger.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Mit diesem Attribut kann eine Anwendung Codierungseigenschaften festlegen, wenn der [Sink Writer](sink-writer.md)verwendet wird. Führen Sie die folgenden Schritte aus, um dieses Attribut festzulegen:

1.  Rufen Sie [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen neuen Eigenschaftenspeicher zu erstellen.
2.  Legen Sie Encodereigenschaften für den Eigenschaftenspeicher fest. Die verfügbaren Eigenschaften hängen vom Encoder ab. Weitere Informationen finden Sie unter [Codec-Objekte.](codecobjects.md)
3.  Rufen Sie [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attributspeicher zu erstellen.
4.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) auf, um den [**IPropertyStore-Zeiger**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für den Attributspeicher festzulegen.
5.  Erstellen Sie eine neue Instanz des Senkenwriters. Übergeben Sie den [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) an die Erstellungsfunktion. Weitere Informationen finden Sie unter [Sink Writer Attributes](sink-writer-attributes.md).

Der Sink Writer legt die Eigenschaften auf dem Encoder fest, bevor die Medientypen festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ÜBERPRÜFENSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Sink Writer-Attribute](sink-writer-attributes.md)
</dt> </dl>

 

 
