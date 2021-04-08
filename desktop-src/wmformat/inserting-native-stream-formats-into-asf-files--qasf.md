---
title: Einfügen von nativen streamformaten in ASF-Dateien (qasf)
description: Einfügen von nativen streamformaten in ASF-Dateien (qasf)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media-Format-SDK, Native Streamformate (qasf)
- Windows Media-Format-SDK, Einfügen von nativen streamformaten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), Einfügen von nativen streamformaten (qasf)
- ASF (Advanced Systems Format), Einfügen von nativen streamformaten (qasf)
- Advanced Systems Format (ASF), Native Streamformate (qasf)
- ASF (Advanced Systems Format), Native Stream-Formate (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Native Streamformate (qasf)
- DirectShow, Einfügen von nativen streamformaten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856692"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Einfügen von nativen streamformaten in ASF-Dateien (qasf)

Standardmäßig erwartet der [WM-ASF-Writer](wm-asf-writer-filter.md) unkomprimierte Audiodaten und Videostreams auf den Eingabe Pins und verwendet das SDK für den Windows Media-Format, um auf die Windows Media Audio und Windows Media Video Codecs zuzugreifen, die die Streams komprimieren. Der ASF-Datei Container kann jedoch für beliebige Datentypen verwendet werden. Durch das Platzieren digitaler Mediendaten in einem ASF-Datei Container können Sie Features hinzufügen, die von ASF bereitgestellt werden, wie z. b. Metadaten und Digital Rights Management (DRM), ohne dass Sie Ihre Inhalte transcodieren müssen.

Zum Erstellen einer ASF-Datei, die Inhalte enthält, die nicht auf Windows Media – basieren, muss die Anwendung den Datenstrom im Filter Diagramm Upstream des WM-ASF-Writers komprimieren und den Komprimierungs Mechanismus des WM-ASF-Writers durch Aufrufen von [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) wie folgt umgehen:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Konfigurieren Sie dann den Filter mit dem gewünschten Profil. Es ist von entscheidender Bedeutung, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt. In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen. Weitere Informationen finden Sie [unter So erstellen Sie ASF-Dateien mithilfe von Drittanbieter-Codecs](to-create-asf-files-using-third-party-codecs.md).

Wenn Sie den WM-ASF-Writer mit dem upstreamfilter verbinden, verwenden Sie die **igraphbuilder:: connectdirect** -Methode. Verwenden Sie keine "Intelligent Connect"-Methoden wie z. b. **igraphbuilder:: Connect** oder **igraphbuilder:: RenderFile** , um den Filter zu verbinden, da dadurch der Modus "Umgehung der Umgehungs Komprimierung" deaktiviert wird.

 

 




