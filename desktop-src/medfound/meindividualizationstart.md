---
description: Wird von der-Richtlinien-Engine ausgelöst, wenn die Individualisierung beginnt. Die Individualisierung wird mithilfe der Anwendungs Implementierung der IMF contentschutzmanager-Schnittstelle durchgeführt.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Meindividualizationstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357455"
---
# <a name="meindividualizationstart-event"></a>Meindividualizationstart-Ereignis

Wird von der-Richtlinien-Engine ausgelöst, wenn die Individualisierung beginnt. Die Individualisierung erfolgt mithilfe der Implementierung der Anwendung der [**imbocontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle.

Eine individualisierte Anwendung ist eine Anwendung, die ein Upgrade auf die Digital Rights Management (DRM)-Komponenten erhalten hat, die Sie von allen anderen Kopien derselben Anwendung unterscheiden. Inhalts Besitzer können verlangen, dass Ihre geschützten Dateien nur in einer Anwendung wiedergegeben werden, die individuell ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn die Lizenz Beschaffung abgeschlossen ist, löst die Richtlinien-Engine das Ereignis " [meindividualizationabgeschlossene](meindividualizationcompleted.md) " aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




