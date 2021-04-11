---
description: Richtlinien zum Registrieren von Filtern
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Richtlinien zum Registrieren von Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed616d90c17d232995994d8ceccfdc72d022d56
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123398"
---
# <a name="guidelines-for-registering-filters"></a>Richtlinien zum Registrieren von Filtern

Die Filter Registrierungsinformationen bestimmen, wie der Filter Graph-Manager während einer [intelligenten Verbindung](intelligent-connect.md)funktioniert. Folglich wirkt sich dies auf jede für DirectShow geschriebene Anwendung aus, nicht nur auf diejenigen, die den Filter verwenden. Stellen Sie sicher, dass sich der Filter ordnungsgemäß verhält, indem Sie diese Richtlinien befolgen.

1.  Benötigen Sie die Filterdaten in der Registrierung? Für viele benutzerdefinierte Filter gibt es keinen Grund, den Filter für den Filter Mapper oder den Enumerator des System Geräts sichtbar zu machen. Solange Sie die dll registrieren, kann Ihre Anwendung den Filter mithilfe von **cokreateinstance** erstellen. Weglassen Sie in diesem Fall einfach die [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur aus der Factory-Vorlage. (Ein Nachteil ist, dass der Filter in GraphEdit nicht angezeigt wird. Um dies zu umgehen, können Sie eine private Test Kategorie mithilfe der [**IFilterMapper2:: anatecategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) -Methode erstellen. Dies sollte nur für Debugbuilds durchzuführen sein.)
2.  Wählen Sie die richtige Filterkategorie aus. Die Standard Kategorie "DirectShow Filters" ist für allgemeine Filter vorgesehen. Registrieren Sie den Filter nach Bedarf in einer spezifischeren Kategorie. Wenn [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) nach einem Filter sucht, werden alle Kategorien ignoriert, deren Verdienst Verdienst \_ \_ nicht \_ oder weniger ist. Kategorien, die nicht für die normale Wiedergabe gedacht sind, haben ein niedriges
3.  Vermeiden Sie die Angabe von MediaType \_ None, mediasubtype \_ None oder GUID \_ NULL in den [**amoviesetup \_ mediaType**](amoviesetup-mediatype.md) -Informationen für eine PIN. **IFilterMapper2** behandelt diese als Platzhalter, wodurch der Diagramm erbauprozess verlangsamt werden kann.
4.  Wählen Sie den geringstmöglichen Wert aus. Im folgenden finden Sie einige Richtlinien:

    | Filtertyp                                                                                       | Empfohlene Leistungen                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Standard-Renderer                                                                                     | \_bevorzugter Vorteil. Für Standard Medientypen sollte ein benutzerdefinierter Renderer jedoch nie der Standardwert sein. |
    | Nicht standardmäßiger Renderer                                                                                 | Das Verdienst wird \_ \_ nicht \_ verwendet oder ist nicht \_ unwahrscheinlich.                                                              |
    | MUX                                                                                                  | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                 |
    | Decoder                                                                                              | Verdienst \_ Normal                                                                                       |
    | Spitter, Parser                                                                                      | Wert \_ Normal oder niedriger                                                                              |
    | Spezieller Filter Alle Filter, die direkt von der Anwendung erstellt werden                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                 |
    | Erfassung                                                                                              | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                 |
    | "Fallback"-Filter; beispielsweise der [Farb Raum Konverter-Filter](color-space-converter-filter.md) | nicht \_ wahrscheinlich                                                                                     |

    

     

    Wenn Sie einen Filter \_ \_ \_ verwenden, bei dem Sie nicht verwenden möchten, sollten Sie überprüfen, ob Sie diese Informationen an erster Stelle registrieren müssen. (Siehe Element 1.)

5.  Registrieren Sie keinen Filter in der Kategorie "DirectShow Filters", die 24-Bit-RGB akzeptiert. Der Filter beeinträchtigt den Farb Raum Konverter-Filter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



