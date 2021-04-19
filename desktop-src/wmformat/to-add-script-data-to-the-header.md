---
title: So fügen Sie dem Header Skript Daten hinzu
description: So fügen Sie dem Header Skript Daten hinzu
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media-Format-SDK, Hinzufügen von Skript Daten zu Headern
- Advanced Systems Format (ASF), Hinzufügen von Skript Daten zu Headern
- ASF (Advanced Systems Format), Hinzufügen von Skript Daten zu Headern
- Skripts, Hinzufügen von Daten zu Headern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106339874"
---
# <a name="to-add-script-data-to-the-header"></a>So fügen Sie dem Header Skript Daten hinzu

Sie können Skript Befehle in den Header einer ASF-Datei einschließen. Um Skript Befehle zum Zeitpunkt der Codierung in den Header zu schreiben, führen Sie die folgenden Schritte aus. Führen Sie diese Schritte vor dem Aufrufen von [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aus.

1.  Abrufen eines Zeigers auf die **iwmheaderinfo** -Schnittstelle durch Aufrufen von **iwmwriter:: QueryInterface**.
2.  Fügen Sie jeden gewünschten Skript Befehl hinzu, indem Sie [**iwmheaderinfo:: addScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript)aufrufen. Bei jedem Aufruf werden die beiden Zeichen folgen separat und die Darstellungs Zeit für den Befehl als Parameter verwendet.

Wenn eine Anwendung die Datei liest, muss Sie alle Skript Befehle abrufen. Führen Sie die folgenden Schritte aus, um alle Skript Befehle im Header einer Datei zu suchen. Dies sollte vor dem Starten der Wiedergabe erfolgen.

1.  Rufen Sie einen Zeiger auf die **iwmheaderinfo** -Schnittstelle des Reader-Objekts (oder des synchronen Reader-Objekts) ab, indem Sie die **QueryInterface** -Methode einer anderen Schnittstelle im-Objekt aufrufen.
2.  Rufen Sie die Gesamtanzahl der Skripts im Header ab, indem Sie [**iwmheaderinfo:: getscriptcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount)aufrufen.
3.  Durchlaufen Sie alle Skripts im Header einzeln mithilfe von Aufrufen von [**iwmheaderinfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Erstellen Sie eine Liste der Präsentations Zeiten, damit Ihre Anwendung zum richtigen Zeitpunkt auf die Befehle reagieren kann.

> [!Note]  
> Wenn Sie DRM zum Verschlüsseln einer Datei verwenden, kann kein Skript Befehl eine Präsentationszeit von 0 aufweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmheaderinfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Verwenden von Skript Befehlen**](using-script-commands.md)
</dt> </dl>

 

 




