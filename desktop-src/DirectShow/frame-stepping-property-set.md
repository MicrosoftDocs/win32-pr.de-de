---
description: Frame Stepping-Eigenschaftensatz
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Frame Stepping-Eigenschaftensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ccddab4cd7f302dc850a4581ce8e70dcffc9cb6a4943c8f768a74c890edfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565000"
---
# <a name="frame-stepping-property-set"></a>Frame Stepping-Eigenschaftensatz

Decoder, die framegenaue Suchfunktionen unter Microsoft DirectShow implementieren, müssen den AM \_ KSPROPSETID \_ FrameStep-Eigenschaftensatz implementieren, der in Verbindung mit der [**IVideoFrameStep-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) verwendet wird.



| Bezeichnung | Wert |
|-------------------|----------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ FrameStep |



 



| Eigenschafts-ID                              | BESCHREIBUNG                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ FRAMESTEP \_ STEP            | Weist den Decoder an, einen Schrittvorgang zu starten, und übergibt eine [**AM \_ PROPERTY \_ FRAMESTEP-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) die die Anzahl der Schritte angibt.            |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL          | Weist den Decoder an, den aktuellen Schrittvorgang abzubrechen. Dieser Eigenschaft sind keine Instanzdaten zugeordnet.                                                                  |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP         | Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass die Frameschritte ausgeführt werden können, \_ andernfalls S FALSE. Es werden keine Instanzdaten übergeben, wenn diese Eigenschaft festgelegt wird.         |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE | Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass er mehrere Frames gleichzeitig schrittweise durchgehen kann, \_ andernfalls S FALSE. Es werden keine Instanzdaten übergeben, wenn diese Eigenschaft festgelegt wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 



