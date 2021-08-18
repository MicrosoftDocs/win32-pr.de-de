---
description: Optionale Streams
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Optionale Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7c30f783a8c13b00020c2dac62cd11e2a79d6f2ea66af01f715c3cb389853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830970"
---
# <a name="optional-streams"></a>Optionale Streams

Ein DMO kann einige ausgabestreams als optional festlegen. Ein optionaler Stream erzeugt Daten, die die Anwendung verwerfen kann, entweder vollständig oder bei gelegentlichen Stichproben. Beispielsweise kann ein optionaler Stream zusätzliche Informationen zu einem primären Stream enthalten.

Um abzufragen, ob ein Stream optional ist, rufen Sie die [**IMediaObject::GetOutputStreamInfo-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) auf, und überprüfen Sie den *parameter pdwFlags.* Optionale Streams geben entweder das DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE-Flag oder das DMO \_ OUTPUT \_ STREAMF \_ OPTIONAL-Flag zurück. Diese Flags bedeuten fast das gleiche. Ein kleiner Unterschied zwischen ihnen wird in Kürze erläutert.

Wenn ein Stream optional ist, kann der Client den DMO anweisen, Daten aus diesem Stream zu verwerfen, wenn er die Ausgabe verarbeitet. Rufen Sie hierzu die [**IMediaObject::P rocessOutput-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) auf, und legen Sie den Ausgabepuffer für jeden Datenstrom, den Sie verwerfen möchten, auf **NULL** fest. (Der Ausgabepuffer wird im **pBuffer-Member** des [**DMO OUTPUT DATA \_ \_ \_ BUFFER**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)angegeben.) Legen Sie außerdem das \_ DMO PROCESS OUTPUT DISCARD WHEN NO \_ \_ \_ \_ \_ BUFFER-Flag im *dwFlags-Parameter* fest.

Für jeden Stream, in dem der *pBuffer-Zeiger* **NULL** ist, versucht der DMO, die Daten zu verwerfen. Wenn der Stream optional ist, verwirft der DMO die Daten garantiert. Wenn der Stream nicht optional ist, verwirft der DMO die Daten nach Möglichkeit, dies ist jedoch nicht garantiert. Wenn die Daten nicht verworfen werden können, wird das flag OUTPUT DATA BUFFERF INCOMPLETE DMO \_ OUTPUT DATA \_ \_ BUFFERF INCOMPLETE \_ festgelegt. Wenn Sie einen *pBuffer-Zeiger* auf **NULL** festlegen, aber das DMO \_ PROCESS OUTPUT DISCARD WHEN NO \_ \_ \_ BUFFER-Flag nicht \_ \_ festlegen, verwirft der DMO die Daten nicht. In diesem Fall puffert der DMO entweder die Ausgabe intern oder schlägt einfach den **ProcessOutput-Aufruf fehl.**

Der einzige funktionale Unterschied zwischen dem DMO \_ OUTPUT \_ STREAMF \_ OPTIONAL-Flag und dem DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE-Flag ist:

-   Das DMO \_ OUTPUT \_ STREAMF \_ OPTIONAL-Flag gibt an, dass der Client keinen Medientyp für diesen Stream festlegen muss. Wenn der Client jedoch mit der Verarbeitung von Daten beginnt, ohne den Medientyp für diesen Stream festzulegen, muss er die Daten für die gesamte Dauer des Streamings aus diesem Stream verwerfen. Wenn Sie Stichproben selektiv verwerfen möchten, müssen Sie den Medientyp festlegen.
-   Das DMO \_ OUTPUT \_ STREAMF \_ DISCARDABLE-Flag gibt an, dass der Stream zwar optional ist, aber immer einen Medientyp erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosten eines DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



