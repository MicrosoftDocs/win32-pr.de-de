---
description: Festlegen von Eigenschaften für die Audioerfassung
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Festlegen von Eigenschaften für die Audioerfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31afe61d4641906391934bafe4c3acb8a911a9fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213803"
---
# <a name="setting-audio-capture-properties"></a>Festlegen von Eigenschaften für die Audioerfassung

Jede Eingabe-PIN im audioerfassungs Filter macht die [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) -Schnittstelle verfügbar. Verwenden Sie diese Schnittstelle, um eine bestimmte Eingabe zu aktivieren bzw. zu deaktivieren, indem Sie die [**IAMAudioInputMixer::p UT- \_ Aktivierungs**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) Methode für die PIN aufrufen. Verwenden Sie diese Schnittstelle auch, um die Eigenschaften einer Eingabe festzulegen, z. b. die Bass-, Treble-und volumeebenen. Wenn Sie mehrere Eingaben gleichzeitig erfassen, können Sie die Gesamtzahl der Bass-, Treble-und volumeebenen über die **IAMAudioInputMixer** -Schnittstelle im Filter selbst steuern.

Die verfügbaren Stichproben Raten und Audioformate für die Erfassung werden vom Treiber bestimmt. Verwenden Sie die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle in der Ausgabe-PIN des audioerfassungs Filters, um die verfügbaren Stichproben Raten und-Formate aufzulisten und das gewünschte Format festzulegen. Der Filter kann eine Downstreamverbindung mit einem beliebigen Filter herstellen, der den Medientyp der Ausgabepin akzeptiert.

Der audioerfassungs Filter macht auch die [**iambufferaushandlung**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) -Schnittstelle verfügbar. Diese Schnittstelle ist nützlich, um die Latenzzeit in der Audiovorschau zu steuern. Standardmäßig verwendet der audioerfassungs Filter eine halbsekunden-Puffergröße. Diese Puffergröße eignet sich optimal für die Erfassung, verursacht jedoch eine Vorschau Verzögerung von einer halben Sekunde. Um die Latenz zu verringern, müssen Sie die [**iambufferaushandlung:: sugerloerproperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) -Methode abrufen, bevor Sie die Ausgabe-PIN des audioerfassungs Filters verbinden. Diese Methode nimmt einen Zeiger auf die Struktur der [**\_ zuordnereigenschaften**](/windows/win32/api/strmif/ns-strmif-allocator_properties) an. Verwenden Sie das **cbbuffer** -Element, um die Puffergröße in Bytes anzugeben. Ein 80 millisekundenpuffer ist im Allgemeinen sicher, aber Puffer mit 30 oder 40 Millisekunden sind möglicherweise ausreichend. Wenn die Puffer zu klein sind, wird die Audioqualität beeinträchtigt.

 

 



