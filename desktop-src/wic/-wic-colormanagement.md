---
description: Die Windows Imaging Component (WIC) vereinfacht die Farbverwaltung durch die Bereitstellung der IWICColorContext-Schnittstelle und der iwiccolortransform-Schnittstelle.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Übersicht über die Farbverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373310"
---
# <a name="color-management-overview"></a>Übersicht über die Farbverwaltung

Digitale Images stammen aus und sind auf eine Vielzahl von Geräten ausgerichtet, die jeweils über einen eigenen Bereich und dynamischen Bereich verfügen. Wenn ein Foto die gleiche Szene auf zwei unterschiedlichen Kameras erfassen würde, werden die Farben in den resultierenden Bildern nicht genau identisch angezeigt, auch wenn Sie auf demselben Ausgabegerät gerendert werden, da sich die Farb Spielfunktionen der beiden Quell Geräte unterscheiden. Ebenso wird dasselbe Bild, das auf zwei verschiedenen Ziel Geräten gerendert wird, anders angezeigt, da die Zielgeräte andere Farbprofile aufweisen. Um eine konsistente Farb Reproduktion zwischen Geräten sicherzustellen, ist es erforderlich, eine Zuordnung zwischen dem Farbprofil des Quell Geräts und dem Farbprofil des Zielgeräts zu erstellen. Die Farbverwaltung versucht, eine enge und konsistente visuelle Übereinstimmung zu schaffen, und ist ein wichtiges Feature bei der professionellen Abbild Erstellung.

Die Möglichkeit, die Farbe über Scanner, Monitore, Drucker und Anwendungen hinweg konsistent zu reproduzieren, klingt wie ein einfaches Ziel, aber ohne ein Farb Verwaltungssystem im Betriebssystem ist es schwierig, dies zu erreichen. Wenn jede Anwendung ihre eigenen Farbprofile generieren muss, ist es fast unmöglich, während des gesamten Veröffentlichungsprozesses einen konsistenten Farb Austausch zu erzielen. dazu gehören das Scannen, bearbeiten und Zusammenführen von Vorgängen, die Absicherung und die Verteilung.

Die Windows Imaging Component (WIC) vereinfacht die Farbverwaltung durch die Bereitstellung der [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Schnittstelle und der [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) -Schnittstelle. Sie können ein [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) -Objekt mithilfe von [**iwicfactory:: foatecolortransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer)erhalten. [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) ist eine Abstraktion für Geräte Farbprofile. **IWICColorContext** wird mit einem BitmapFrame, dem Farbprofil des Quell Geräts und dem Farbprofil des Zielgeräts initialisiert. Er führt die Konvertierung des bitmapframes aus.

 

 



