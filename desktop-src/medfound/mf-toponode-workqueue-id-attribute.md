---
description: Gibt eine Arbeits Warteschlange für eine topologieverzweigung an.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130137"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>ID-Attribut der MF- \_ toponode- \_ workqueue \_

Gibt eine Arbeits Warteschlange für eine topologieverzweigung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**). Das-Attribut ist optional.

Der Wert des-Attributs ist ein von der Anwendung definierter Bezeichner für die Arbeits Warteschlange.

Anwendungen können dieses Attribut verwenden, um den branches der Topologie Arbeits Warteschlangen zuzuweisen. Jeder Quellknoten in der Topologie definiert eine Verzweigung. Die Verzweigung schließt jeden topologieknoten ein, der Daten von diesem Knoten empfängt.

Wenn Sie dieses Attribut festlegen, müssen Sie die [**imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) -Methode für die aufgelöste Topologie aufrufen. Mehrere Verzweigungen in der Topologie können dieselbe Arbeits Warteschlange gemeinsam verwenden, und Arbeits Warteschlangen können über Topologien hinweg wieder verwendet werden.

> [!Note]  
> Der Wert dieses Attributs ist nicht mit dem Bezeichner identisch, der von der MF-Funktion der [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) -Funktion zurückgegeben wird. Der Wert des-Attributs ist ein von der Anwendung definierter Bezeichner, der zum Zuordnen von topologiebranches zu Arbeits Warteschlangen verwendet wird. Wenn die Medien Sitzung eine neue Arbeits Warteschlange belegt, speichert Sie den tatsächlichen Bezeichner der Arbeits Warteschlange intern.

 

Wenn dieses Attribut festgelegt wird, kann die Anwendung die Verzweigung auch einer MMCSS-Aufgabe (Multimedia Class Scheduler Service) zuweisen, indem das Attribut " [**MF \_ toponode \_ workqueue \_ MMCSS \_ Class**](mf-toponode-workqueue-mmcss-class-attribute.md) " festgelegt wird.

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

[**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> </dl>

 

 




