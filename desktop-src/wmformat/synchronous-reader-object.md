---
title: Synchrones Reader-Objekt
description: Synchrones Reader-Objekt
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Medienformat-SDK, synchrone Readerobjekte
- Advanced Systems Format (ASF), synchrone Readerobjekte
- ASF (Advanced Systems Format), synchrone Readerobjekte
- Objekte,synchrone Readerobjekte
- Synchrone Reader,Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629f08684f996a611acaf00b913eaa8715869bdfd0219ea27994e2f8faf7c896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197060"
---
# <a name="synchronous-reader-object"></a>Synchrones Reader-Objekt

Das synchrone Readerobjekt wird verwendet, um digitale Mediendateien mit synchronen Aufrufen zu lesen.

Das synchrone Readerobjekt wird von der [**Funktion WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)erstellt, die einen Zeiger auf eine **IWMSyncReader-Schnittstelle** legt. Die anderen Schnittstellen, die von der synchronen Readerschnittstelle unterstützt werden, können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom synchronen Readerobjekt unterstützt.



| Schnittstelle                                | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Legt Headerinformationen wie Metadaten, Marker [](wmformat-glossary.md)und so weiter fest und ruft sie ab.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumeriert die verfügbaren Codecinformationen. Erbt alle Methoden von **IWMHeaderInfo.**                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Unterstützt große Attributgrößen, doppelte Attributnamen und Unterstützung mehrerer Sprachen. Erbt alle Methoden von **IWMHeaderInfo** und **IWMHeaderInfo2.** |
| [**IWMProfile**](iwmprofile.md)         | Ermöglicht den Zugriff auf die Profilinformationen der Windows Mediendatei, die in den Reader geladen wurde.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Ruft den guiD (Globally Unique Identifier) ab, sofern dieser dem Profil zugeordnet ist. Erbt alle Methoden von **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Unterstützt die Gemeinsame Nutzung von Bandbreiten und Streampriorisierungsinformationen im Profil. Erbt alle Methoden von **IWMProfile** und **IWMProfile2.**                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Bietet synchrone Lesefunktionen für digitale Mediendateien.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Bietet Unterstützung für das Suchen nach SMPTE-Zeitcodes und das manuelle Zuordnen von Beispielen. Erbt alle Methoden von **IWMSyncReader.**                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




