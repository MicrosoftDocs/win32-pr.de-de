---
description: Gibt an, ob Topologien eine globale Start-und Endzeit haben.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: MF_SESSION_GLOBAL_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362336"
---
# <a name="mf_session_global_time-attribute"></a>\_ \_ Globales \_ Zeit Attribut der MF-Sitzung

Gibt an, ob Topologien eine globale Start-und Endzeit haben.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut festlegen, wenn Sie das Medium "sesison" mit dem *pconfiguration* -Parameter der Funktion " [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) " oder " [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) " erstellen.

Wenn dieses Attribut vorhanden und ungleich NULL ist, müssen alle Topologien, die an die Medien Sitzung übermittelt werden, über das Projekt " [**MF \_ Topology \_ ProjectStart**](mf-topology-projectstart-attribute.md) " und " [**MF \_ Topology \_ projectstoppt**](mf-topology-projectstop-attribute.md) " verfügen. Diese Attribute geben die Start-und Endzeit Zeiten für die Topologie relativ zur gesamten Präsentation an.

Wenn dieses Attribut nicht vorhanden oder **falsch** ist, dürfen die Topologien nicht über das Projekt für die [**MF- \_ TopologieTopologie \_ ProjectStart**](mf-topology-projectstart-attribute.md) oder die [**MF- \_ Topologie \_ projectstoppt**](mf-topology-projectstop-attribute.md) verfügen.

Verwenden Sie dieses Attribut, um Bearbeitungs Sequenzen zu erstellen. Weitere Informationen finden Sie unter [Sequenz Präsentations Zeiten](sequence-presentation-times.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medien Sitzungs Attribute](media-session-attributes.md)
</dt> <dt>

[Sequenz Präsentations Zeiten](sequence-presentation-times.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**MF- \_ Topologie \_ ProjectStart**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**MF- \_ Topologie \_ projectstoppt**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




