---
description: Sammeln von Fine-Tuning Informationen
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Sammeln von Fine-Tuning Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346185"
---
# <a name="collecting-fine-tuning-information"></a>Sammeln von Fine-Tuning Informationen

Obwohl normalerweise eine exakte Kabel Frequenz erwartet wird, können Broadcast Häufigkeiten von der Broadcast Station nach oben oder unten angepasst werden, um potenzielle Störungen durch benachbarte Kanäle zu verringern.

Wenn der TV-Tuner die Genauigkeit eines Kanals filtert, sucht er nach dem genauesten Signal. Gehen Sie folgendermaßen vor, um diese Informationen für nachfolgende Optimierungs Vorgänge in der Registrierung zu speichern:

1.  Nennen Sie [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) , um den Bereich der Häufigkeits Einträge in der Tabelle Current Frequency zu bestimmen.
2.  Nennen Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) einmal für jeden Häufigkeits Index im Bereich.
3.  Wenden Sie [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) an, um die Informationen zur Feinabstimmung in der Registrierung zu speichern. Die Informationen werden unter dem Registrierungsschlüssel für den aktuellen Optimierungs Bereich gespeichert.

Diese Schritte sind im folgenden Code dargestellt:


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



Bei früheren Versionen des TV-Tuner-Filters wurde die [**iamtvtuner:: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) -Methode für die Feinabstimmung empfohlen. Diese Methode ignoriert jedoch alle Häufigkeits Überschreitungen, sodass ihre Verwendung nicht mehr empfohlen wird. Der folgende Code entspricht der **Autotune** -Methode, funktioniert aber ordnungsgemäß mit Häufigkeits Überschreitungen:


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



Beim Broadcast Empfang ist es nicht immer möglich, eine horizontale Sperre zu erhalten, obwohl das Bild angezeigt werden kann. In diesen Fällen erhält die Tuner-Hardware eine Häufigkeits Sperre, aber der Decoder hat keine horizontale Sperre. Diese Bedingung kann erkannt werden, wenn Sie " [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) " oder " [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) " durch Untersuchen des Rückgabecodes verwenden.



| Wert    | BESCHREIBUNG                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK    | Der Tune-Vorgang war erfolgreich, und der Tuner hat eine Häufigkeits Sperre erhalten.                                                                                                                          |
| S \_ false | Während des Tune-Vorgangs sind keine Fehler aufgetreten, aber der Tuner konnte keine Häufigkeits Sperre erhalten. Es ist sehr unwahrscheinlich, dass es einen sichtbaren Kanal gibt, der aus diesem Vorgang resultiert. |



 

Jeder andere Rückgabecode gibt an, dass ein Fehler aufgetreten ist.

Der Rückgabewert S \_ OK garantiert nicht, dass der Decoder über eine horizontale Sperre verfügt. Die [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) -Methode aktualisiert den *foundsignal* -Parameter, um anzugeben, ob eine horizontale Sperre erreicht wurde. Die [**iamtuner:: signalpresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) -Methode gibt die gleichen Informationen zurück.

Wenn der Rückgabewert S OK ist, kann \_ die Anwendung jedoch den *foundsignal* -Parameter ignorieren, da der Tuner eine Häufigkeits Sperre meldet. Es besteht die Möglichkeit einer Häufigkeits Sperre für Rauschen. diese Möglichkeit sollte jedoch gegen die Möglichkeit abgewogen werden, sichtbare Kanäle zu überspringen.

## <a name="registry-conversion"></a>Registrierungs Konvertierung

Zur Unterstützung von Überschreibungs Überschreitungen hat sich das interne Format des Registrierungsschlüssels, der Informationen zur Feinabstimmung enthält, geändert. Das ursprüngliche Format wird weiterhin aus Gründen der Abwärtskompatibilität unterstützt, unterstützt jedoch keine Häufigkeits Überschreitungen.

Das alte Registrierungs Format wird immer dann in das neue Format konvertiert, wenn die [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) -Methode aufgerufen wird. Wenn Ihre Anwendung Häufigkeits Überschreitungen hinzufügt, sollte Sie die **storeautotune** -Methode zum Konvertieren in das neue Registrierungs Format abrufen. Vor dem Aufruf von **storeautotune** müssen keine fein Optimierungs Informationen erfasst werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Analog-TV-Optimierung](international-analog-tv-tuning.md)
</dt> </dl>

 

 



