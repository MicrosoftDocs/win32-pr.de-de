---
description: Richtlinien für das Registrieren von Filtern
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Richtlinien für das Registrieren von Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221cadf6fb4806a2fa5c5b2cc4fd9abf423cec426ec23cd76b0bc642080852af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905360"
---
# <a name="guidelines-for-registering-filters"></a>Richtlinien für das Registrieren von Filtern

Die Filterregistrierungsinformationen bestimmen, wie der Filter Graph Manager während [intelligent Verbinden](intelligent-connect.md)funktioniert. Daher wirkt sie sich auf jede Für DirectShow geschriebene Anwendung aus, nicht nur auf dieJenigen, die Ihren Filter verwenden. Sie sollten sicherstellen, dass sich Ihr Filter ordnungsgemäß verhält, indem Sie diese Richtlinien befolgen.

1.  Benötigen Sie die Filterdaten in der Registrierung? Bei vielen benutzerdefinierten Filtern gibt es keinen Grund, den Filter für den Filterzuordnungs- oder Systemgeräte-Enumerator sichtbar zu machen. Solange Sie die DLL registrieren, kann Ihre Anwendung den Filter mit **CoCreateInstance** erstellen. In diesem Fall müssen Sie einfach die [**AMOVIESETUP \_ FILTER-Struktur**](amoviesetup-filter.md) aus der Factoryvorlage weglassen. (Ein Nachteil ist, dass Ihr Filter in GraphEdit nicht sichtbar ist. Um dies zu umgehen, können Sie eine private "Testing"-Kategorie mit der [**IFilterMapper2::CreateCategory-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) erstellen. Dies sollten Sie nur für Debugbuilds durchführen.)
2.  Wählen Sie die richtige Filterkategorie aus. Die Standardkategorie "DirectShow-Filter" ist für allgemeine Filter vorgesehen. Registrieren Sie Ihren Filter nach Bedarf in einer spezifischeren Kategorie. Wenn [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) nach einem Filter sucht, werden alle Kategorien ignoriert, deren Vorteile NICHT USE \_ oder weniger \_ \_ sind. Kategorien, die nicht für die normale Wiedergabe vorgesehen sind, haben geringe Vorteile.
3.  Vermeiden Sie die Angabe von MEDIATYPE \_ None, MEDIASUBTYPE \_ None oder GUID \_ NULL in den [**AMOVIESETUP \_ MEDIATYPE-Informationen**](amoviesetup-mediatype.md) für einen Pin. **IFilterMapper2** behandelt diese als Platzhalter, was den Grapherstellungsprozess verlangsamen kann.
4.  Wählen Sie den niedrigsten möglichen Wert aus. Hier sind einige Richtlinien:

    | Filtertyp                                                                                       | Empfohlene Leistung                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Standardrenderer                                                                                     | DIES \_ IST VORZUZIEHEN. Bei Standardmedientypen sollte ein benutzerdefinierter Renderer jedoch nie die Standardeinstellung sein. |
    | Nicht standardmäßiger Renderer                                                                                 | DIES IST \_ UNWAHRSCHEINLICH, WENN DIES \_ NICHT \_ DER FALL IST. \_                                                              |
    | Mux                                                                                                  | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                 |
    | Decoder                                                                                              | NORMALER WERT \_                                                                                       |
    | Spitter, Parser                                                                                      | VORZEICHEN \_ NORMAL oder niedriger                                                                              |
    | Filter für spezielle Zwecke; Filter, die direkt von der Anwendung erstellt werden                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                 |
    | Erfassung                                                                                              | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                 |
    | Filter "Fallback"; z. B. der [Farbraumkonverterfilter](color-space-converter-filter.md) | \_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT                                                                                     |

    

     

    Wenn Sie einem Filter einen Vorteil von "NEED \_ \_ DO NOT \_ USE" geben, sollten Sie überlegen, ob Sie diese Informationen überhaupt registrieren müssen. (Siehe Element 1.)

5.  Registrieren Sie keinen Filter in der Kategorie "DirectShow-Filter", der 24-Bit-RGB akzeptiert. Ihr Filter beeinträchtigt den Filter Farbraumkonverter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



