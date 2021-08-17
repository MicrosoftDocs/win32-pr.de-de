---
title: Verwalten der Paketgröße
description: Verwalten der Paketgröße
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Medienformat-SDK, Verwalten von Paketgrößen
- Windows Medienformat-SDK, Paketgrößen
- Profile,Paketgrößen
- Profile,Verwalten von Paketgrößen
- Packets,sizes
- packets,IWMPacketSize-Schnittstelle
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b8755eccdcc0042532be4359cd51fce2ef379b51882e6cc4585c48c8769a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846712"
---
# <a name="managing-packet-size"></a>Verwalten der Paketgröße

Der Writer wurde entwickelt, um die Größe von Paketen intern zu verwalten. Möglicherweise gelten jedoch bestimmte Anforderungen für Ihre Anwendung, die eine manuelle Kontrolle über die Größe der Pakete in den von Ihnen geschriebenen ASF-Dateien erforderlich machen. Das Windows Media Format SDK stellt zwei Schnittstellen bereit: [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) und [**IWMPacketSize2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) mit denen Sie die maximale und minimale Größe von Paketen steuern können.

Beide Paketgrößenschnittstellen werden im Profilobjekt verfügbar gemacht. Sie sind auch für das Readerobjekt verfügbar. Wie bei anderen profilbezogenen Schnittstellen kann der Reader nur auf die Lesemethoden zugreifen.

Die Größe der Pakete wirkt sich auf die Leistung aus. Im Allgemeinen gilt: Je kleiner die Paketgröße, desto fragmentierter sind die Daten in einer Datei. Wenn eine Datei fragmentierter ist, desto weniger effizient ist es, sie zu rekonstruieren. In einem Streamingszenario ist dies möglicherweise kein wichtiger Aspekt, da der Prozess zum Lesen einer Datei aus einer Internetquelle im Allgemeinen ineffizient ist. Wenn Sie eine Datei lokal verwenden, kann dies jedoch eine Überlegung sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPacketSize-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**IWMPacketSize2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




