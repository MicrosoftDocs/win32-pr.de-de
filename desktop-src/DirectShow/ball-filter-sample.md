---
description: Beispiel für Ballfilter
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Beispiel für Ballfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df215f6f4be5fa1bc94872ac4e5855d4e9c0f19a136708d0c9377b19c5d79dda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084540"
---
# <a name="ball-filter-sample"></a>Beispiel für Ballfilter

## <a name="description"></a>BESCHREIBUNG

Der Ball-Filter ist ein Videoquellfilter, der ein Bild einer Hüpfkugel erzeugt. Dieses Beispiel veranschaulicht die Formataushandlung und die Verwendung der Quellfilter-Basisklassen [**CSource**](csource.md) und [**CSourceStream.**](csourcestream.md)

Der Code in Fball.h und Fball.cpp verwaltet die Filterschnittstellen. Diese beiden Dateien enthalten ungefähr den minimalen Code, der für einen Quellfilter erforderlich ist. Die Dateien "Ball.h" und "Ball.cpp" enthalten den Code, der die Kugel springt.

Dieser Filter verfügt über einen einzelnen Ausgabepin, der einen Videostream bereitstellt, der zeigt, wie eine Kugel im Frame springt. Der Ball-Filter akzeptiert auch Qualitätsverwaltungsanforderungen vom Downstreamfilter, was eine einfache Strategie für das Qualitätsmanagement veranschaulicht. Dieser Filter implementiert zu diesem Zweck die [**IQualityControl-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: \[ *SDK Root* \] \\ Samples Multimedia \\ \\ DirectShow \\ Filters \\ Ball.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



