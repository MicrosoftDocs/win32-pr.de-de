---
description: Wird von der-Richtlinien-Engine ausgelöst, wenn der Lizenzerwerb beginnt. Der Lizenzerwerb erfolgt mithilfe der Anwendungs Implementierung der imbocontentschutzmanager-Schnittstelle.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Melicenmenacquisitionstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356606"
---
# <a name="melicenseacquisitionstart-event"></a>Melicenmenacquisitionstart-Ereignis

Wird von der-Richtlinien-Engine ausgelöst, wenn der Lizenzerwerb beginnt. Der Lizenzerwerb erfolgt mithilfe der Implementierung der Anwendung der [**imbocontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn die Lizenz Erfassung abgeschlossen ist, löst die Richtlinien-Engine das Ereignis " [melicenabacquisitionabgeschlossene](melicenseacquisitioncompleted.md) " aus.

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

 

 




