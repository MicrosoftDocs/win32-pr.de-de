---
description: Gibt eine Arbeitswarteschlange für eine Topologieverzweigung an.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ba4ab55d2a70b4b0c081544ab43a78719fab537fbf478519bde1e65dfc9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955090"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ ID-Attribut

Gibt eine Arbeitswarteschlange für eine Topologieverzweigung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Das Attribut ist optional.

Der Wert des Attributs ist ein anwendungsdefinierter Bezeichner für die Arbeitswarteschlange.

Anwendungen können dieses Attribut verwenden, um Verzweigungen der Topologie Arbeitswarteschlangen zuzuweisen. Jeder Quellknoten in der Topologie definiert einen Branch. Der Branch enthält jeden Topologieknoten, der Daten von diesem Knoten empfängt.

Wenn Sie dieses Attribut festlegen, rufen Sie die [**METHODE MENUWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) für die aufgelöste Topologie auf. Mehrere Branches in der Topologie können dieselbe Arbeitswarteschlange gemeinsam nutzen, und Arbeitswarteschlangen können topologieübergreifend wiederverwendet werden.

> [!Note]  
> Der Wert dieses Attributs entspricht nicht dem Bezeichner, der von der [**MFAllocateWorkQueue-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) zurückgegeben wird. Der Wert des Attributs ist ein anwendungsdefinierter Bezeichner und wird verwendet, um Topologiebranches Arbeitswarteschlangen zuzuordnen. Wenn die Mediensitzung eine neue Arbeitswarteschlange zuordnet, wird der tatsächliche Arbeitswarteschlangenbezeichner intern gespeichert.

 

Wenn dieses Attribut festgelegt ist, kann die Anwendung den Branch auch einer MMCSS-Aufgabe (Multimedia Class Scheduler Service) zuweisen, indem sie das [**\_ MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS-Attribut**](mf-toponode-workqueue-mmcss-class-attribute.md) festlegt.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MENUWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS-KLASSE \_**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeitswarteschlangen](work-queues.md)
</dt> </dl>

 

 




