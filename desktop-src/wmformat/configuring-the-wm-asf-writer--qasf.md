---
title: Konfigurieren von WM ASF Writer (qasf)
description: Konfigurieren von WM ASF Writer (qasf)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media-Format-SDK, Konfigurieren von WM-ASF-Writer (qasf)
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, WM-ASF-Writer
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), Konfigurieren von WM ASF Writer (qasf)
- ASF (Advanced Systems Format), Konfigurieren von WM ASF Writer (qasf)
- Advanced Systems Format (ASF), WM-ASF-Writer
- ASF (Advanced Systems Format), WM-ASF-Writer
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, Konfigurieren von WM-ASF-Writer (qasf)
- DirectShow, WM-ASF-Writer
- DirectShow, qasf
- WM-ASF-Writer, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102147"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Konfigurieren von WM ASF Writer (qasf)

Wenn der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter erstellt wird, wird er automatisch mit dem wmprofile \_ V80 256- \_ Video Profil als Standard konfiguriert. Da für dieses Profil die Codecs Windows Media Audio und Windows Media Video Version 8 verwendet werden, empfiehlt es sich, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und dann seinen [**iwmprofile**](iwmprofile.md) -Zeiger mithilfe der [**iconfigasfwriter::**](iconfigasfwriter-configurefilterusingprofile.md) Configuration Report profile-Methode an den Filter zu übergeben. Der Filter muss dem Diagramm hinzugefügt werden, bevor der Filter konfiguriert werden kann, und er muss konfiguriert werden, bevor er mit upstreamfiltern verbunden werden kann. Der Filter verwendet das Profil, um zu bestimmen, welche Art von Windows Media-Format Datei geschrieben werden soll, wie viele Eingabe Pins eingerichtet werden und welche Medientypen von den Pins akzeptiert werden können.

Der Filter ermöglicht das Zurücksetzen von Profilen, während die Eingabe Pins verbunden sind, solange das neue Profil keine zusätzlichen Eingabe Pins erfordert. Wenn Sie z. b. das Profil aus einem reinen Audioprofil in ein zweidimensionales Audio-und Video Profil ändern, muss nur die audiopin mit einem Zeitstempel versehen werden, und alle Eingabe Pins müssen verbunden sein, bevor der Filter ausgeführt oder angehalten werden kann. Dies bedeutet Folgendes: Wenn Sie den Filter mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter eine Audioeingabe-PIN und eine Videoeingabe-PIN. beide Pins müssen miteinander verbunden sein, bevor der Filter ausgeführt werden kann.

Hinzufügen von Dateneinheiten Erweiterungen

Sie können einen profilstream für dateneinheits Erweiterungen konfigurieren, wie z. b. SMPTE-Zeit Codes, entweder vor oder nach dem Verbinden des Filters, solange Sie dieser Reihenfolge von Vorgängen folgen:

1.  Fügen Sie dem Stream mithilfe von [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)eine oder mehrere Dateneinheiten Erweiterungen hinzu.
2.  [**Wmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) zum Aktualisieren des Profils aufruft.
3.  Nennen Sie [**iconfigasfwriter:: konfigurierfilterusingprofile**](iconfigasfwriter-configurefilterusingprofile.md) mit dem aktualisierten Profil Objekt.
4.  Suchen Sie die Videoeingabe-PIN, und wenden Sie Ihre [**iamwmbufferpass:: setnotify**](iamwmbufferpass-setnotify.md) -Methode an, um Ihre Anwendungs definierte [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle zu registrieren.

Wenn das Diagramm ausgeführt wird, wird die [**iamwmbufferpasscallback:: notify**](iamwmbufferpasscallback-notify.md) -Methode für jeden Frame aufgerufen, und Sie können Eigenschaften für das Beispiel mithilfe der [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstellen Methoden erhalten und festlegen.

> [!Note]  
> In einigen Prozessor intensiven Szenarien wie z. b. Inverse Telecine benötigt der WM-ASF-Writer möglicherweise mehr Ausgabepuffer, als von einigen downstreamfiltern unterstützt werden kann. Der DV-Decoder nimmt z. b. für die Ausgabepin nicht mehr als einen Puffer an, und dasselbe gilt für den AVI-Dekompressor unter bestimmten Bedingungen. Wenn beim Versuch, eine Verbindung mit diesen Filtern herzustellen, oder möglicherweise beim Ausführen des Diagramms Probleme auftreten, kann es erforderlich sein, einen Vermittler Filter zu schreiben, der eine beliebige Anzahl von Puffern in der Ausgabe-PIN akzeptiert.

 

 

 