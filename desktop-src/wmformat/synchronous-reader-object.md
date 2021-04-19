---
title: Synchrones Reader-Objekt
description: Synchrones Reader-Objekt
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media-Format-SDK, synchrone Reader-Objekte
- Advanced Systems Format (ASF), synchrone Reader-Objekte
- ASF (Advanced Systems Format), synchrone Reader-Objekte
- Objekte, synchrone Reader-Objekte
- synchrone Reader, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106337212"
---
# <a name="synchronous-reader-object"></a>Synchrones Reader-Objekt

Das synchrone Reader-Objekt wird zum Lesen digitaler Mediendateien mithilfe von synchronen Aufrufen verwendet.

Das synchrone Reader-Objekt wird von der [**wmkreatesynkreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)-Funktion erstellt, die einen Zeiger auf eine **iwmsynkreader** -Schnittstelle festlegt. Die anderen von der synchronen Reader-Schnittstelle unterstützten Schnittstellen können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom synchronen Reader-Objekt unterstützt.



| Schnittstelle                                | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Legt Header Informationen, wie z. b. Metadaten, [*Marker*](wmformat-glossary.md)usw., fest und ruft Sie ab.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Listet die verfügbaren Codec-Informationen auf. Erbt alle Methoden von **iwmheaderinfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Unterstützt umfangreiche Attribut Größen, doppelte Attributnamen und Unterstützung mehrerer Sprachen. Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**. |
| [**Iwmprofile**](iwmprofile.md)         | Ermöglicht den Zugriff auf die Profilinformationen der in den Reader geladenen Windows-Mediendatei.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Ruft die Globally Unique Identifier (GUID) ab, die dem Profil zugeordnet ist, sofern vorhanden. Erbt alle Methoden von **iwmprofile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Unterstützt die Bandbreiten Freigabe und Datenstrom Priorisierungs Informationen im Profil. Erbt alle Methoden von **iwmprofile** und **IWMProfile2**.                |
| [**Iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Stellt synchrone Lesefunktionen für digitale Mediendateien bereit.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Bietet Unterstützung für das Durchsuchen von SMPTE-Zeit Codes und das manuelle Zuordnen von Beispielen. Erbt alle Methoden von **iwmsynkreader**.                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




