---
description: Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem laufenden System installieren.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aktualisieren eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349983"
---
# <a name="updating-a-provider"></a>Aktualisieren eines Anbieters

Manchmal müssen Sie möglicherweise eine neuere Version eines Anbieters auf einem laufenden System installieren. Wenn Ihr Anbieter als DLL installiert ist, können Sie einen neuen Anbieter installieren, ohne den Dienst neu starten zu müssen, den Computer neu starten oder andere Anwendungen, die WMI verwenden, zu diesem Zeitpunkt anderweitig beeinflussen können.

Im folgenden Verfahren wird beschrieben, wie ein-Anbieter aktualisiert wird.

**So aktualisieren Sie einen Anbieter**

1.  Erstellen Sie den neuen Anbieter.

    1.  Kompilieren Sie den neuen Anbieter mit einem anderen DLL-Namen und einer anderen **CLSID**.

        Ändern Sie beispielsweise Myprov.dll in Myprov1.dll und **CLSID \_ myproprov** in **CLSID \_ MyProv** 1.

    2.  Ändern Sie die MOF-Datei für die Anbieter Registrierung so, dass Sie die neue CLSID (CLSID \_ MyProv1), jedoch den gleichen Anbieter Namen ("MyProv") verwendet.

2.  Installieren Sie den neuen Anbieter.

    1.  Kopieren Sie die neue Anbieter-DLL zusammen mit dem neuen Namen.
    2.  Registrieren Sie den neuen Anbieter selbst.

        Verwenden Sie z. b. den **regsvr32** **myprov1.dll** -Befehl, um den neuen Anbieter zu registrieren.

    3.  Kompilieren Sie die neue MOF-Anbieter Registrierung, wodurch die alte Anbieter Registrierung überschrieben wird. Bis zu diesem Punkt war der alte Anbieter voll funktionsfähig. der neue Anbieter ist nun voll funktionstüchtig.

3.  Entfernen Sie ggf. die alte Version des Anbieters.

    1.  Heben Sie die Registrierung der alten dll auf.

        Verwenden Sie z. b. den **regsvr32** **/#b0-** Befehl, um die Registrierung der alten dll aufzuheben.

    2.  Markieren Sie die alte dll, die beim Neustart gelöscht werden soll, indem Sie " [**muvefileex**](/windows/desktop/api/winbase/nf-winbase-movefileexa)" aufrufen.

Sie können ähnliche Schritte ausführen, um ein Upgrade eines von einem lokalen Server implementierten Anbieters durchzuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
