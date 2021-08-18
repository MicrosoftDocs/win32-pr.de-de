---
title: Einfügen nativer Streamformate in ASF-Dateien (QASF)
description: Einfügen nativer Streamformate in ASF-Dateien (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Medienformat-SDK, native Streamformate (QASF)
- Windows Medienformat-SDK, Einfügen nativer Streamformate in ASF-Dateien (QASF)
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF), Einfügen nativer Streamformate (QASF)
- ASF (Advanced Systems Format), Einfügen nativer Streamformate (QASF)
- Advanced Systems Format (ASF), native Streamformate (QASF)
- ASF (Advanced Systems Format), native Streamformate (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, native Streamformate (QASF)
- DirectShow,Einfügen nativer Streamformate in ASF-Dateien (QASF)
- Windows Medienformat-SDK, QASF
- Advanced Systems Format (ASF), QASF
- ASF (Advanced Systems Format), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b395748520943a62645a88c018131f909577191ebafbe1f9c4d3a80219cb39f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701777"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Einfügen nativer Streamformate in ASF-Dateien (QASF)

Standardmäßig erwartet WM [ASF Writer](wm-asf-writer-filter.md) unkomprimierte Audio- und Videostreams auf den Eingabepins und verwendet das Windows Media Format SDK, um auf die Windows Medienaudio- und Windows Media Video-Codecs zuzugreifen, die die Streams komprimieren. Der ASF-Dateicontainer kann jedoch für jeden Datentyp verwendet werden. Indem Sie digitale Mediendaten in einem ASF-Dateicontainer platzieren, können Sie von ASF bereitgestellte Features wie Metadaten und DRM (Digital Rights Management) hinzufügen, ohne Ihre Inhalte transcodieren zu müssen.

Um eine ASF-Datei zu erstellen, die Inhalte enthält, die nicht Windows medienbasiert sind, muss die Anwendung den Stream im Filterdiagramm vor dem WM ASF Writer komprimieren und den Komprimierungsmechanismus des WM ASF Writer umgehen, indem [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) wie folgt aufgerufen wird:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Konfigurieren Sie dann den Filter mit dem gewünschten Profil. Es ist wichtig, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt. In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen. Weitere Informationen finden Sie unter [So erstellen Sie ASF-Dateien mithilfe von Codecs von Drittanbietern.](to-create-asf-files-using-third-party-codecs.md)

Wenn Sie den WM ASF Writer mit dem Upstreamfilter verbinden, verwenden Sie die **IGraphBuilder::ConnectDirect-Methode.** Verwenden Sie keine "intelligent connect"-Methoden wie **IGraphBuilder::Verbinden** oder **IGraphBuilder::RenderFile,** um den Filter zu verbinden, da dadurch der Modus "Bypass Compression" des Filters deaktiviert wird.

 

 




