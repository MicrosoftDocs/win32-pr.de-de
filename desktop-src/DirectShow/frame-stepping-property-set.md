---
description: Frame Step-Eigenschaften Satz
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Frame Step-Eigenschaften Satz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746640"
---
# <a name="frame-stepping-property-set"></a>Frame Step-Eigenschaften Satz

Decoderer, die Frame-exakte Suchvorgänge unter Microsoft DirectShow implementieren, müssen den "am \_ kspropsetid"- \_ framestep-Eigenschafts Satz implementieren, der in Verbindung mit der [**ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) -Schnittstelle verwendet wird.



|                   |                            |
|-------------------|----------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropabtid- \_ framestep |



 



| Eigenschafts-ID                              | BESCHREIBUNG                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM- \_ Eigenschafts \_ framestep- \_ Schritt            | Weist den Decoder an, einen Schritt Vorgang zu starten, und übergibt eine [**am \_ Property \_ framestep**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) -Struktur, die die Anzahl von Schritten angibt.            |
| AM \_ Eigenschaften \_ framestep \_ Abbrechen          | Weist den Decoder an, den aktuellen Schritt Vorgang abzubrechen. Dieser Eigenschaft sind keine Instanzdaten zugeordnet.                                                                  |
| AM, \_ Eigenschaften \_ framestep, \_ canstep         | Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass er Frame-Stepping ausführen kann, \_ andernfalls false. Wenn diese Eigenschaft festgelegt ist, werden keine Instanzdaten übermittelt.         |
| AM \_ Property \_ framestep \_ canstepmultiple | Der Decoder gibt s \_ OK für diese Anweisung zurück, um anzugeben, dass er mehrere Frames gleichzeitig ausführen kann, \_ andernfalls false. Wenn diese Eigenschaft festgelegt ist, werden keine Instanzdaten übermittelt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 



