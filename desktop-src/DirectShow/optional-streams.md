---
description: Optionale Streams
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Optionale Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340069"
---
# <a name="optional-streams"></a>Optionale Streams

Ein DMO kann einige seiner Ausgabedaten Ströme als optional festlegen. Ein optionaler Stream erzeugt Daten, die von der Anwendung verworfen werden können, entweder vollständig oder bei gelegentlichen Stichproben. Ein optionaler Stream kann z. b. zusätzliche Informationen über einen primären Stream enthalten.

Um abzufragen, ob ein Stream optional ist, müssen Sie die [**imediaobject:: getoutputstreaminfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) -Methode aufrufen und den *pdwflags* -Parameter überprüfen. Optionale Streams geben entweder das Flag "DMO \_ Output \_ streamf \_ verwerdable" oder das \_ optionale Flag "DMO Output \_ streamf" zurück \_ . Diese Flags bedeuten fast dieselbe Sache: ein kleiner Unterschied zwischen Ihnen wird in Kürze erläutert.

Wenn ein Datenstrom optional ist, kann der Client den DMO anweisen, Daten aus diesem Stream zu verwerfen, wenn die Ausgabe verarbeitet wird. Dazu müssen Sie die [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) -Methode und den Ausgabepuffer für jeden Datenstrom, den Sie verwerfen möchten, auf **null** festlegen. (Der Ausgabepuffer wird im **pbuffer** -Member des [**DMO- \_ Ausgabe \_ Daten \_ Puffers**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)angegeben.) Legen Sie außerdem die DMO- \_ Prozess \_ Ausgabe \_ verwerfen, \_ Wenn \_ kein \_ pufferflag im *dwFlags* -Parameter enthalten ist.

Für jeden Stream, bei dem der *pbuffer* -Zeiger **null** ist, versucht der DMO, die Daten zu verwerfen. Wenn der Stream optional ist, werden die Daten von DMO garantiert verworfen. Wenn der Datenstrom nicht optional ist, verwirft DMO die Daten, wenn möglich, dies ist jedoch nicht garantiert. Wenn die Daten nicht verworfen werden können, wird das Flag "DMO \_ Output \_ Data \_ bufferf unvollständig" festgelegt \_ . Wenn Sie einen *pbuffer* -Zeiger auf **null** festlegen, aber die DMO- \_ Prozess \_ Ausgabe \_ verwerfen \_ \_ , wenn kein \_ pufferflag festgelegt ist, werden die Daten von DMO nicht verworfen. In diesem Fall puffert der DMO die Ausgabe entweder intern, oder es wird einfach der **ProcessOutput** -Befehl fehlgeschlagen.

Der einzige funktionale Unterschied zwischen dem optionalen Flag der DMO \_ -ausgabestreamf und dem debugfähigen \_ \_ DMO- \_ ausgabeablaufflag \_ lautet wie \_ folgt:

-   Das \_ optionale Flag DMO Output \_ streamf \_ gibt an, dass der Client keinen Medientyp für diesen Stream festlegen muss. Wenn der Client jedoch mit der Verarbeitung von Daten beginnt, ohne den Medientyp für diesen Stream festzulegen, muss er die Daten aus diesem Stream für die gesamte Dauer des Streamings verwerfen. Wenn Sie die Beispiele selektiv verwerfen möchten, müssen Sie den Medientyp festlegen.
-   Das Flag für die DMO-Ausgabe-streamf-abreservierung gibt an, \_ \_ \_ dass, obwohl der Stream optional ist, immer ein Medientyp erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosting eines DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



