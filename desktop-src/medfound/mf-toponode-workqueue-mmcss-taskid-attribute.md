---
description: Gibt einen MMCSS-Taskbezeichner (Multimedia Class Scheduler Service) für einen Topologiezweig an.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf75dc911c9d00cab2d21d937ef16a43b38cc4271299c6fae4f2ed7381ec63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739628"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID-Attribut

Gibt einen MMCSS-Taskbezeichner (Multimedia Class Scheduler Service) für einen Topologiezweig an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Dieses Attribut ist optional.

Dieses Attribut wird ignoriert, es sei denn, die folgenden Attribute sind ebenfalls festgelegt:

-   [**\_ \_ MF-TOPONODE-WORKQUEUE-ID \_**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS-KLASSE \_**](mf-toponode-workqueue-mmcss-class-attribute.md)

Wenn die Anwendung einen ihrer eigenen Threads bei MMCSS registriert, können Sie dieses Attribut verwenden, um die Topologiearbeitswarteschlange der MMCSS-Gruppe der Anwendung zu zuordnen. Legen Sie den Attributwert auf den Taskbezeichner fest, den die Anwendung bei der Registrierung bei MMCSS empfangen hat. (Der Taskbezeichner wird im *TaskIndex-Parameter* der [**AvSetMmThreadCharacteristics-Funktion**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) zurückgegeben. Weitere Informationen finden Sie im Thema [Prozess- und Threadfunktionen](../procthread/process-and-thread-functions.md).)

Wenn MMCSS einen neuen Taskbezeichner für die Topologie zuweisen soll, legen Sie das [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS-Attribut**](mf-toponode-workqueue-mmcss-class-attribute.md) fest, aber nicht das **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID-Attribut.**

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**REGISTRWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeitswarteschlangen](work-queues.md)
</dt> </dl>

 

 
