---
description: DMO Mindestanforderungen
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO Mindestanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc4f664d32112512120f2f20687051a0bff193e00adb7ad595e6975c522fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749140"
---
# <a name="dmo-minimum-requirements"></a>DMO Mindestanforderungen

Jede DMO sollte die folgenden Mindestanforderungen erfüllen:

-   Die Aggregation muss unterstützt werden.
-   Sie muss die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) verfügbar machen.
-   Das Threadingmodell muss "beide" sein. DMOs müssen in einer Freethreadumgebung ordnungsgemäß funktionieren.

Audioeffekt-DMOs sollten die [**IMediaObjectInPlace-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) für die Verwendung in DirectObject und DirectSound unterstützen.

Die folgenden Schnittstellen sind an anderer Stelle dokumentiert, sind aber für viele DMOs nützlich. Sie sind jedoch nicht erforderlich.

-   **ISpecifyPropertyPages**, **IPropertyPage:** Diese Schnittstellen ermöglichen es einem DMO, eine Eigenschaftenseite für den Benutzer zum Festlegen von Eigenschaften zur Verfügung zu stellen.
-   **IPersistStream:** Diese Schnittstelle ermöglicht dem DMO, seinen Zustand im persistenten Speicher zu speichern.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression:**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)Diese Schnittstellen ermöglichen es einem Client, das Ausgabeformat und die Komprimierungseinstellungen eines Encoders zu konfigurieren. (Diese beiden Schnittstellen sind Teil der DirectShow-API, werden aber auch für DMOs empfohlen.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 



