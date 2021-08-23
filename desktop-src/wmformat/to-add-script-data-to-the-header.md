---
title: So fügen Sie dem Header Skriptdaten hinzu
description: So fügen Sie dem Header Skriptdaten hinzu
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Medienformat-SDK, Hinzufügen von Skriptdaten zu Headern
- Advanced Systems Format (ASF), Hinzufügen von Skriptdaten zu Headern
- ASF (Advanced Systems Format), Hinzufügen von Skriptdaten zu Headern
- Skripts, Hinzufügen von Daten zu Headern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a8ad34a69427dc26435a6a599b8d91db2ebe2b8be700483189b2e7ba22846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027318"
---
# <a name="to-add-script-data-to-the-header"></a>So fügen Sie dem Header Skriptdaten hinzu

Sie können Skriptbefehle in den Header einer ASF-Datei einschließen. Führen Sie die folgenden Schritte aus, um skriptbefehle zum Zeitpunkt der Codierung in den Header zu schreiben. Führen Sie diese Schritte aus, bevor [**Sie IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aufrufen.

1.  Rufen Sie einen Zeiger auf die **IWMHeaderInfo-Schnittstelle** ab, indem **Sie IWMWriter::QueryInterface** aufrufen.
2.  Fügen Sie jeden gewünschten Skriptbefehl hinzu, indem [**Sie IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript)aufrufen. Jeder Aufruf verwendet die beiden Zeichenfolgen getrennt und die Präsentationszeit, die für den Befehl als Parameter verwendet werden soll.

Wenn eine Anwendung die Datei liest, müssen alle Skriptbefehle abgerufen werden. Führen Sie die folgenden Schritte aus, um alle Skriptbefehle im Header einer Datei zu suchen. Dies sollte vor dem Starten der Wiedergabe erfolgen.

1.  Rufen Sie einen Zeiger auf die **IWMHeaderInfo-Schnittstelle** des Readerobjekts (oder des synchronen Readerobjekts) ab, indem Sie die **QueryInterface-Methode** einer anderen Schnittstelle im -Objekt aufrufen.
2.  Rufen Sie [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount)auf, um die Gesamtanzahl der Skripts im Header abzurufen.
3.  Durchlaufen Sie alle Skripts im Header einzeln, indem Sie Aufrufe von [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript)verwenden.
4.  Erstellen Sie eine Liste der Präsentationszeiten, damit Ihre Anwendung zum richtigen Zeitpunkt auf die Befehle reagieren kann.

> [!Note]  
> Wenn Sie DRM zum Verschlüsseln einer Datei verwenden, kann kein Skriptbefehl eine Präsentationszeit von 0 aufweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMHeaderInfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Verwenden von Skriptbefehlen**](using-script-commands.md)
</dt> </dl>

 

 




