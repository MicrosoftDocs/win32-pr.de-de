---
title: Konfigurieren des WM ASF Writer (QASF)
description: Konfigurieren des WM ASF Writer (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Medienformat-SDK, Konfigurieren von WM ASF Writer (QASF)
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, WM ASF Writer
- Windows Medienformat-SDK, QASF
- Advanced Systems Format (ASF), Konfigurieren von WM ASF Writer (QASF)
- ASF (Advanced Systems Format), Konfigurieren von WM ASF Writer (QASF)
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (Advanced Systems Format), WM ASF Writer
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), QASF
- ASF (Advanced Systems Format), QASF
- DirectShow,Konfigurieren von WM ASF Writer (QASF)
- DirectShow,WM ASF Writer
- DirectShow, QASF
- WM ASF Writer,Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4559fc1780bdb9a9b398471cc842e2f3cf46f9c84a483229b01b3b6fa4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199176"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Konfigurieren des WM ASF Writer (QASF)

Wenn der [WM ASF Writer-Filter](wm-asf-writer-filter.md) erstellt wird, wird er automatisch mit dem WMProfile \_ V80 \_ 256Video-Profil als Standard konfiguriert. Da dieses Profil die Codecs Windows Media Audio und Windows Media Video Version 8 verwendet, wird empfohlen, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und dann den [**IWMProfile-Zeiger**](iwmprofile.md) mithilfe der [**IConfigAsfWriter::ConfigureFilterUsingProfile-Methode**](iconfigasfwriter-configurefilterusingprofile.md) an den Filter zu übergeben. Der Filter muss dem Diagramm hinzugefügt werden, bevor der Filter konfiguriert werden kann, und er muss konfiguriert werden, bevor er mit Upstreamfiltern verbunden werden kann. Der Filter verwendet das Profil, um zu bestimmen, welche Art von Windows Medienformatdatei geschrieben werden soll, wie viele Eingabepins eingerichtet werden müssen und welche Medientypen die Pins akzeptieren können.

Der Filter ermöglicht das Zurücksetzen von Profilen, während die Eingabepins verbunden sind, solange für das neue Profil keine zusätzlichen Eingabepins erforderlich sind. Wenn Sie z. B. das Profil von einem Profil mit nur einer Eingabe in ein Audio- und Videoprofil mit zwei Eingaben ändern, wird nur der Audioanschluss erneut verbundenAlle Eingabedaten müssen mit einem Zeitstempel versehen sein, und alle Eingabepins müssen verbunden werden, bevor der Filter ausgeführt oder angehalten werden kann. Wenn Sie den Filter also mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter eine Audio- und einen Videoeingabepin, und beide Pins müssen verbunden werden, bevor der Filter ausgeführt werden kann.

Hinzufügen von Dateneinheiterweiterungen

Sie können einen Profildatenstrom für Dateneinheiterweiterungen konfigurieren, z. B. SMPTE-Zeitcodes, entweder vor oder nach dem Verbinden des Filters, sofern Sie diese Reihenfolge von Vorgängen befolgen:

1.  Fügen Sie dem Stream mithilfe von [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)eine oder mehrere Dateneinheitserweiterungen hinzu.
2.  Rufen Sie [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) auf, um das Profil zu aktualisieren.
3.  Rufen Sie [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) mit dem aktualisierten Profilobjekt auf.
4.  Suchen Sie den Videoeingabepin, und rufen Sie die [**zugehörige IAMWMBufferPass::SetNotify-Methode**](iamwmbufferpass-setnotify.md) auf, um Ihre anwendungsdefinierte [**IAMWMBufferPassCallback-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) zu registrieren.

Wenn das Diagramm ausgeführt wird, wird ihre [**IAMWMBufferPassCallback::Notify-Methode**](iamwmbufferpasscallback-notify.md) für jeden Frame aufgerufen, und Sie können Eigenschaften für das Beispiel mithilfe der [**INSSBuffer3-Schnittstellenmethoden**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) abrufen und festlegen.

> [!Note]  
> In einigen prozessorintensiven Szenarien, z. B. inverse Telekope, benötigt WM ASF Writer möglicherweise mehr Ausgabepuffer, als einige Downstreamfilter unterstützen können. Der DV-Decoder akzeptiert z. B. nicht mehr als einen Puffer für seinen Ausgabepin, und das gleiche gilt für den AVI-Dekomprimierer unter bestimmten Bedingungen. Wenn beim Versuch, eine Verbindung mit diesen Filtern herzustellen, oder möglicherweise beim Ausführen des Graphen Probleme auftreten, ist es möglicherweise erforderlich, einen Zwischenfilter zu schreiben, der eine beliebige Anzahl von Puffern auf dem Ausgabepin akzeptiert.

 

 

 