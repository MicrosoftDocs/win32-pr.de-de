---
description: Mindestens erforderliche DMO-Anforderungen
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Mindestens erforderliche DMO-Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957995"
---
# <a name="dmo-minimum-requirements"></a>Mindestens erforderliche DMO-Anforderungen

Jeder DMO sollte die folgenden Mindestanforderungen erfüllen:

-   Die Aggregation muss unterstützt werden.
-   Es muss die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar machen.
-   Das Threading Modell muss "both" lauten. DMOS muss in einer frei Hand Thread Umgebung ordnungsgemäß funktionieren.

Der Audioeffekt-DMOS sollte die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle unterstützen, die in DirectMusic und DirectSound verwendet werden kann.

Die folgenden Schnittstellen sind an anderer Stelle dokumentiert, sind aber für viele DMOS nützlich. Sie sind jedoch nicht erforderlich.

-   **ISpecifyPropertyPages**, **IPropertyPage**: Diese Schnittstellen ermöglichen es einem DMO, eine Eigenschaften Seite bereitzustellen, damit Benutzereigenschaften festlegen können.
-   **IPersistStream**: Diese Schnittstelle ermöglicht es dem DMO, seinen Zustand in einem persistenten Speicher zu speichern.
-   [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): Diese Schnittstellen ermöglichen es einem Client, das Ausgabeformat und die Komprimierungs Einstellungen eines Encoders zu konfigurieren. (Diese beiden Schnittstellen sind Teil der DirectShow-API, werden aber auch für DMOS empfohlen.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



