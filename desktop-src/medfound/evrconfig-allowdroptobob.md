---
description: Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung mithilfe von Bob Deinterlacing zu verbessern.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: EVRConfig_AllowDropToBob-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393266"
---
# <a name="evrconfig_allowdroptobob-attribute"></a>Evrconfig \_ allowdroptybob-Attribut

Ermöglicht dem erweiterten Videorenderer (EVR), die Leistung mithilfe von Bob Deinterlacing zu verbessern.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann für die evrmedia-Senke festgelegt werden. Um das Attribut festzulegen, wird **QueryInterface** zum Abfragen der EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle festgelegt.

Das Festlegen dieses Attributs hat dieselbe Auswirkung wie das Festlegen des " **MF videomixprefs \_ allowdroptybob** "-Flags für den EVR. Eine Beschreibung dieses Flags finden Sie unter [**MF videomixprefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .

Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Video Qualitäts Verwaltung](video-quality-management.md)
</dt> </dl>

 

 




