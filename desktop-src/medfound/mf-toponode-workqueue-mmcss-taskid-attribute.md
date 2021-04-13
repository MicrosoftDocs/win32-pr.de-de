---
description: Gibt einen MMCSS-Task Bezeichner (Multimedia Class Scheduler Service) für eine topologieverzweigung an.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527410"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID-Attribut

Gibt einen MMCSS-Task Bezeichner (Multimedia Class Scheduler Service) für eine topologieverzweigung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**). Dieses Attribut ist optional.

Dieses Attribut wird ignoriert, es sei denn, die folgenden Attribute werden ebenfalls festgelegt:

-   [**MF- \_ toponode- \_ workwarteschlangen- \_ ID**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**](mf-toponode-workqueue-mmcss-class-attribute.md)

Wenn die Anwendung einen ihrer eigenen Threads mit MMCSS registriert, können Sie dieses Attribut verwenden, um die topologiearbeitswarteschlange der MMCSS-Gruppe der Anwendung zuzuordnen. Legen Sie den Attribut Wert auf den Task Bezeichner fest, den die Anwendung bei der Registrierung bei MMCSS erhalten hat. (Der Task Bezeichner wird im *Taskindex* -Parameter der [**avsetmmthreadcharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) -Funktion zurückgegeben. Weitere Informationen finden Sie im Thema [Prozess-und Thread Funktionen](../procthread/process-and-thread-functions.md).)

Wenn MMCSS einen neuen Task Bezeichner für die Topologie zuweisen soll, legen Sie das Attribut [**MF \_ toponode \_ workqueue \_ MMCSS \_ Class**](mf-toponode-workqueue-mmcss-class-attribute.md) fest, aber legen Sie das Attribut **MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID** nicht fest.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> </dl>

 

 
