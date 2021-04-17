---
title: Verwalten der Paketgröße
description: Verwalten der Paketgröße
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media-Format-SDK, Verwalten von Paketgrößen
- Windows Media-Format-SDK, Paketgrößen
- Profile, Paketgrößen
- Profile, Verwalten von Paketgrößen
- Pakete, Größen
- Pakete, iwmpacketsize-Schnittstelle
- Iwmpacketsize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390055"
---
# <a name="managing-packet-size"></a>Verwalten der Paketgröße

Der Writer ist darauf ausgelegt, die Größe von Paketen intern zu verwalten. Möglicherweise haben Sie jedoch spezielle Anforderungen an Ihre Anwendung, die eine manuelle Steuerung der Größe von Paketen in den von Ihnen geschriebenen ASF-Dateien erfordern. Das Windows Media-Format SDK bietet zwei Schnittstellen, [**iwmpacketsize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) und [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , mit denen Sie die maximale und minimale Größe von Paketen steuern können.

Beide Schnittstellen für die Paketgröße werden im Profil Objekt verfügbar gemacht. Sie sind auch für das Reader-Objekt verfügbar. Wie bei anderen Profil bezogenen Schnittstellen kann der Reader nur auf die Lesemethoden zugreifen.

Die Größe von Paketen wirkt sich auf die Leistung aus. Im Allgemeinen wird die Größe der Daten in einer Datei mit der geringeren Paketgröße fragmentiert. Wenn eine Datei stärker fragmentiert ist, desto weniger effizient wird Sie erstellt. In einem Streamingszenario ist dies möglicherweise kein wichtiger Aspekt, da das Lesen einer Datei aus einer Internet Quelle im allgemeinen ineffizient ist. Beim lokalen Umgang mit einer Datei ist dies jedoch möglicherweise ein Aspekt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpacketsize-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**IWMPacketSize2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




