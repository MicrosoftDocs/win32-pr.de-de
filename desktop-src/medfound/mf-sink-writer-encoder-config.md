---
description: Enthält einen Zeiger auf einen Eigenschaften Speicher mit Codierungs Eigenschaften.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757399"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>Konfigurations Attribut für den MF- \_ \_ senderwriter \_ \_

Enthält einen Zeiger auf einen Eigenschaften Speicher mit Codierungs Eigenschaften.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger.

Dieses Attribut ermöglicht es einer Anwendung, Codierungs Eigenschaften festzulegen, wenn der [Senke-Writer](sink-writer.md)verwendet wird. Führen Sie die folgenden Schritte aus, um dieses Attribut festzulegen:

1.  Rufen Sie [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen neuen Eigenschaften Speicher zu erstellen.
2.  Legen Sie die Codierungs Eigenschaften für den Eigenschaften Speicher fest. Die verfügbaren Eigenschaften hängen vom Encoder ab. Weitere Informationen finden Sie unter [Codec-Objekte](codecobjects.md).
3.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.
4.  Aufrufen von [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , um den [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger auf den Attribut Speicher festzulegen.
5.  Erstellen Sie eine neue Instanz des Senke Writers. Übergeben Sie den [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger an die Erstellungs Funktion. Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).

Der senkwriter legt die Eigenschaften für den Encoder vor dem Festlegen der Medientypen fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imbersink Writer**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> </dl>

 

 
