---
description: Legt die Basisthreadpriorität für den Quelllese- oder Senkenwriter fest.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY-Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740602"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>MF \_ READWRITE \_ MMCSS \_ PRIORITY-Attribut

Legt die Basisthreadpriorität für den Quelllese- oder Senkenwriter fest.

## <a name="data-type"></a>Datentyp

**INT32** als **UINT32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Legen Sie dieses Attribut optional fest, wenn Sie eine Instanz des [Quelllesers](source-reader.md) oder [des Senkenwriters](sink-writer.md)erstellen. Wenn Sie dieses Attribut festlegen, legen Sie auch das [MF \_ READWRITE \_ MMCSS \_ CLASS-Attribut](mf-readwrite-mmcss-class.md) fest. Andernfalls wird dieses Attribut ignoriert.

Wenn der Quelllese- oder Senkenwriter Threads beim [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md)registriert, gibt der Wert dieses Attributs die Basisthreadpriorität an. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
