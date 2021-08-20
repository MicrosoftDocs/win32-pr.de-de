---
title: Writer-Push-Senkenobjekt
description: Writer-Push-Senkenobjekt
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Medienformat-SDK,Writer-Pushsenkeobjekte
- Advanced Systems Format (ASF), Writer-Pushsenkeobjekte
- ASF (Advanced Systems Format), Writer push sink objects
- Objekte,Writer-Pushsenkeobjekte
- Writer-Pushsenkenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859e4d2d5cf2530e655b74705b1d6f9ef93960d28f523c00e0da7a7336ab258d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006330"
---
# <a name="writer-push-sink-object"></a>Writer-Push-Senkenobjekt

Das Writer-Pushsenkenobjekt verteilt digitale Medien an Veröffentlichungspunkte. Beispielsweise kann ein Live-Concert von einem einzelnen Server codiert und dann an mehrere andere Server übermittelt oder per Push übertragen werden, die den Inhalt an Benutzer streamen.

Ein Writer-Pushsenkenobjekt wird von der [**Funktion WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)erstellt, die einen Zeiger auf eine **IWMWriterPushSink-Schnittstelle** legt. Die anderen vom -Objekt unterstützten Schnittstellen, die in der folgenden Tabelle aufgeführt sind, können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Ermöglicht es der Anwendung, Statusmeldungen aus dem -Objekt zu erhalten.                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Verwaltet eine Pushverteilungssitzung.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und macht mehrere Rückruffunktionen verfügbar. |



 

Die folgende Rückrufschnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writer-Pushsenkenobjekts zu verfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Hostanwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Senden von ASF-Daten an einen Veröffentlichungspunkt**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




