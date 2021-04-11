---
description: Gibt die Codierungsqualität für die Digital Living Network Alliance (DLNA)-Medien Senke an.
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: MF_MP2DLNA_ENCODE_QUALITY-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042342"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>MF \_ MP2DLNA \_ \_ Qualitäts Attribut codieren

Gibt die Codierungsqualität für die Digital Living Network Alliance (DLNA)-Medien Senke an.

## <a name="data-type"></a>Datentyp

**UINT32**

Bereich: 0 – 18

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Höhere Zahlen weisen auf eine bessere Codierungsqualität hin. Niedrigere Zahlen weisen auf eine schnellere Codierung hin, aber eine niedrigere Codierungsqualität. Der Standardwert ist 9.

Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab. Legen Sie das-Attribut vor Beginn des Streamings fest.

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

 

 




