---
description: Festlegen von Audioaufnahmeeigenschaften
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Festlegen von Audioaufnahmeeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078810"
---
# <a name="setting-audio-capture-properties"></a>Festlegen von Audioaufnahmeeigenschaften

Jeder Eingabepin im Audioaufnahmefilter macht die [**IAMAudioInputMixer-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) verfügbar. Verwenden Sie diese Schnittstelle, um eine bestimmte Eingabe zu aktivieren oder zu deaktivieren, indem Sie die [**IAMAudioInputMixer::p ut \_ Enable-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) für den Pin aufrufen. Verwenden Sie diese Schnittstelle auch zum Festlegen von Eigenschaften einer Eingabe, z. B. der Pegel "1", "Treble" und "Volume". Wenn Sie mehrere Eingaben gleichzeitig erfassen, können Sie über die **IAMAudioInputMixer-Schnittstelle** für den Filter selbst die Gesamtebenen "3" und "Treble" steuern.

Die verfügbaren Samplingraten und Audioformate für die Erfassung werden vom Treiber bestimmt. Verwenden Sie [**die IAMStreamConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) auf dem Ausgabepin des Audioaufnahmefilters, um die verfügbaren Samplingraten und -formate aufzählen und das gewünschte Format festlegen. Der Filter kann eine Downstream-Verbindung mit jedem Filter herstellen, der den Medientyp des Ausgabepins akzeptiert.

Der Audioaufnahmefilter macht auch die [**IAMBufferNegotiation-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) verfügbar. Diese Schnittstelle ist nützlich, um die Latenz in der Audiovorschau zu steuern. Standardmäßig verwendet der Audioaufnahmefilter eine Puffergröße von einer halben Sekunde. Diese Puffergröße ist für die Erfassung optimal, verursacht jedoch eine Vorschauverzögerung von einer Halben Sekunde. Um die Latenz zu reduzieren, rufen Sie die [**IAMBufferNegotiation::SuggestAllocatorProperties-Methode**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) auf, bevor Sie den Ausgabepin des Audioerfassungsfilters verbinden. Diese Methode verwendet einen Zeiger auf die [**ALLOCATOR \_ PROPERTIES-Struktur.**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Verwenden Sie **den cbBuffer-Member,** um die Puffergröße in Bytes anzugeben. Ein Puffer von 80 Millisekunden ist im Allgemeinen sicher, aber Puffer von 30 oder 40 Millisekunden können ausreichend sein. Wenn die Puffer zu klein sind, wird die Soundqualität beeinträchtigt.

 

 



