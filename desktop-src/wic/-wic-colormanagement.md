---
description: Windows Die Bildverarbeitungskomponente (Imaging Component, WIC) vereinfacht die Farbverwaltung, indem die IWICColorContext-Schnittstelle und die IWICColorTransform-Schnittstelle zur Verfügung gestellt werden.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Übersicht über die Farbverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a8c30074210a0a061fcbd26b05054591d2023805bfdff0848f0d7054dfe07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090049"
---
# <a name="color-management-overview"></a>Übersicht über die Farbverwaltung

Digitale Bilder stammen von und sind auf eine Vielzahl von Geräten ausgerichtet, von denen jedes über einen eigenen gamut- und dynamischen Bereich verfügt. Wenn ein Zuschauer die gleiche Szene auf zwei verschiedenen Kameras erfassen würde, würden die Farben in den resultierenden Bildern nicht genau gleich aussehen, auch wenn sie auf demselben Ausgabegerät gerendert wurden, da die Farbskalafunktionen der beiden Quellgeräte unterschiedlich waren. Ebenso wird das gleiche Bild, das auf zwei verschiedenen Zielgeräten gerendert wird, unterschiedlich angezeigt, da die Zielgeräte unterschiedliche Farbprofile aufweisen. Um eine konsistente Farbwiedergabe zwischen Geräten sicherzustellen, muss eine Zuordnung vom Farbprofil des Quellgeräts zum Farbprofil des Zielgeräts erstellt werden. Die Farbverwaltung versucht, eine enge und konsistente visuelle Übereinstimmung zu erzielen, und ist ein wichtiges Feature bei der professionellen Bildverarbeitung.

Die Möglichkeit, Farben über Scanner, Monitore, Drucker und Anwendungen hinweg konsistent zu reproduzieren, klingt wie ein einfaches Ziel, aber ohne ein Farbverwaltungssystem im Betriebssystem ist es schwierig zu erreichen. Wenn jede Anwendung ihre eigenen Farbprofile generieren muss, ist es fast unmöglich, während des gesamten Veröffentlichungsprozesses einen konsistenten Farbaustausch zu erreichen, einschließlich Überprüfung, Bearbeitung und Komposition, Proofing und Verteilung.

Windows Die Bildverarbeitungskomponente (Imaging Component, WIC) vereinfacht die Farbverwaltung, indem die [**IWICColorContext-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) und die [**IWICColorTransform-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) zur Verfügung gestellt werden. Sie können ein [**IWICColorTransform-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) mithilfe von [**IWICFactory::CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer)abrufen. [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) ist eine Abstraktion für das Gerätefarbprofil. **IWICColorContext** wird mit einem Bitmaprahmen, dem Farbprofil des Quellgeräts und dem Farbprofil des Zielgeräts initialisiert. Er führt die Konvertierung des Bitmapframes aus.

 

 



