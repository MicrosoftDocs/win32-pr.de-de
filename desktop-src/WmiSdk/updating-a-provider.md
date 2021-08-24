---
description: Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem ausgeführten System installieren.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aktualisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8c40a3d50672115478ae62135774f5a1aad93373bd5b844402e89462b44fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757650"
---
# <a name="updating-a-provider"></a>Aktualisieren eines Anbieters

Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem ausgeführten System installieren. Wenn Ihr Anbieter als DLL installiert ist, können Sie einen neuen Anbieter installieren, ohne den Dienst neu starten, den Computer neu starten oder sich anderweitig auf Anwendungen auswirken zu müssen, die WMI zu diesem Zeitpunkt verwenden.

Im folgenden Verfahren wird beschrieben, wie sie einen Anbieter aktualisieren.

**So aktualisieren Sie einen Anbieter**

1.  Erstellen Sie den neuen Anbieter.

    1.  Kompilieren Sie den neuen Anbieter mit einem anderen DLL-Namen und einer anderen **CLSID.**

        Ändern Sie beispielsweise Myprov.dll in Myprov1.dll und **CLSID \_ MyProProv** in **CLSID \_ MyProv** 1.

    2.  Ändern Sie die MOF-Datei für die Anbieterregistrierung so, dass die neue CLSID (CLSID MyProv1), aber derselbe \_ Anbietername ("MyProv") verwendet wird.

2.  Installieren Sie den neuen Anbieter.

    1.  Kopieren Sie die neue Anbieter-DLL mit dem neuen Namen neben der alten.
    2.  Registrieren Sie den neuen Anbieter selbst.

        Verwenden Sie beispielsweise den Befehl **regsvr32** **myprov1.dll,** um den neuen Anbieter zu registrieren.

    3.  Kompilieren Sie die mof-Datei für die neue Anbieterregistrierung, und überschreiben Sie dadurch die alte Anbieterregistrierung. Bis zu diesem Zeitpunkt war der alte Anbieter voll funktionsfähig. jetzt ist der neue Anbieter voll funktionsfähig.

3.  Entfernen Sie bei Bedarf die alte Version des Anbieters.

    1.  Aufheben der Registrierung der alten DLL.

        Verwenden Sie beispielsweise den Befehl **regsvr32** **/umyprov.dll,** um die Registrierung der alten DLL zu aufheben.

    2.  Markieren Sie die alte DLL, die beim Neustart gelöscht werden soll, indem Sie [**MoveFileEx aufrufen.**](/windows/desktop/api/winbase/nf-winbase-movefileexa)

Sie können ähnliche Schritte ausführen, um einen vom lokalen Server implementierten Anbieter zu aktualisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
