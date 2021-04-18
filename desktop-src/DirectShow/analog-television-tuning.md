---
description: Optimierung des analogen Fernseh ERS
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Optimierung des analogen Fernseh ERS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343949"
---
# <a name="analog-television-tuning"></a>Optimierung des analogen Fernseh ERS

Die Optimierung wird durch den TV-Tuner-Filter über die [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) -Schnittstelle gesteuert. Die iamtvtuner-Schnittstelle erbt iamtuner. Um einen Zeiger auf die-Schnittstelle zu erhalten, rufen Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode wie folgt auf:


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



Der erste Parameter gibt an, dass Upstream aus dem Erfassungs Filter gesucht werden soll.

Häufigkeits Tabellen

Intern speichert der TV-Tuner-Filter eine Liste der Häufigkeits Tabellen. Jede Häufigkeits Tabelle entspricht der Broadcast-oder Kabel Frequenz für ein bestimmtes Land bzw. eine bestimmte Region. Es gibt auch eine generische "Unicable"-Häufigkeits Tabelle, die verwendet wird, wenn ein Land/eine Region keinen Standardsatz von Häufigkeits Zuweisungen hat.

Jede Häufigkeits Tabelle enthält eine Liste von Optimierungs Frequenzen. In einigen Ländern bzw. Regionen entsprechen die Indizes in der Tabelle direkt den channelnummern – mit anderen Worten, die Häufigkeit für Channel n ist der n-ten Eintrag in der Tabelle. Für einige Länder/Regionen gibt es jedoch keine direkte Entsprechung zwischen Kanalnummern und Frequenzen. In diesem Fall muss die Anwendung eine Liste behalten, in der Kanalnummern (in der Regel vom Benutzer ausgewählt) für Häufigkeits Tabelleneinträge zugeordnet werden. Beispielsweise kann der Benutzer, der als "Channel 5" angezeigt wird, in der Tabelle "Frequency" die Einstiegsnummer 12 aufweisen.

Weitere Informationen finden Sie unter [internationale analoge TV-](international-analog-tv-tuning.md)Optimierung.

Grundlegende Optimierungs Vorgänge

Wenn der Tuner mehrere Empfangsmodi unterstützt, z. b. TV und FM Radio, wenden Sie [**iamtuner::p UT- \_ Modus**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) an, um den Modus auszuwählen. Die [**iamtuner:: getavailablemodes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) -Methode gibt alle Modi zurück, die der Tuner unterstützt. Mit dem folgenden Code wird beispielsweise überprüft, ob der TUNER FM Radio unterstützt. wenn dies der Fall ist, wechselt er in diesen Modus.


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



Um das Land/die Region festzulegen, nennen Sie die [**iamtuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) -Methode. Der Tuner verwendet diesen Wert, um die geeignete Häufigkeits Tabelle auszuwählen. Weitere Informationen finden Sie unter [Land/Region-Zuweisungen](country-region-assignments.md) .

Um den Kanal festzulegen, wenden Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) an. Das Argument für diese Methode ist keine Channelnummer, sondern ein Index in der aktuellen Häufigkeits Tabelle. Wie bereits beschrieben, entspricht die Indexnummer möglicherweise einer Kanalnummer. Die [**iamtuner:: channelminmax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) -Methode gibt die minimalen und maximalen Indexwerte für die aktuelle Frequency-Tabelle zurück.

Überschreibungs Häufigkeits Einträge

Möglicherweise sind einige Einträge in den Häufigkeits Tabellen falsch oder veraltet. Daher wird ein Mechanismus zum Überschreiben einzelner Einträge mithilfe von Registrierungs Schlüsseln bereitgestellt.

Einzelheiten hierzu finden Sie im Thema [internationale analoge TV-](international-analog-tv-tuning.md)Optimierung. Jeder Registrierungsschlüssel definiert einen "Optimierungs Bereich", der einen oder mehrere Unterschlüssel enthält. Jeder Unterschlüssel überschreibt einen Häufigkeits Eintrag. Um den aktuellen Optimierungs Bereich festzulegen, verwenden Sie die [**iamtuner::p UT \_ tuningspace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) -Methode. Wenn Sie den Optimierungs Bereich aktivieren, werden die Häufigkeits Einträge in der Tabelle Current Frequency überschrieben. Daher besteht die Anwendung darin, eine Entsprechung zwischen den Optimierungs Bereichen und Ländern bzw. Regionen beizubehalten. Die beste Vorgehensweise besteht darin, den Land-/Regionsbezeichner als Namen für den Optimierungs Bereich zu verwenden.

Optimieren der Häufigkeits Einträge

Übertragungs Häufigkeiten können von der Broadcast Station mehrere kHz nach oben oder unten angepasst werden, um potenzielle Störungen durch benachbarte Kanäle zu verringern. Aufgrund der nominalen Häufigkeit kann die Tuner-Karte die genaue Häufigkeit überprüfen. Der TV-Tuner-Filter verfügt über einen Mechanismus zum Speichern der angepassten Frequenzen in der Registrierung.

Für jeden Eintrag in der Frequency-Tabelle wird die Put \_ Channel-Methode aufgerufen, um diese Häufigkeit zu optimieren. Der Tuner scannt die präzisere Häufigkeit. Sie können überprüfen, ob der Tuner durch Aufrufen von [**iamtuner:: signalpresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent)eine horizontale Sperre erreicht hat. Der TV-Tuner-Filter speichert das Ergebnis auch intern.

Nachdem Sie alle Frequenzen überprüft haben, wenden Sie die [**iamtvtuner:: storeautotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) -Methode an, um die aktualisierten Werte in die Registrierung zu schreiben. Die aktualisierten Werte werden unter dem Registrierungs Eintrag für den aktuellen Optimierungs Bereich gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Analog Fernsehen](analog-television.md)
</dt> </dl>

 

 



