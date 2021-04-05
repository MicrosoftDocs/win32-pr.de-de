---
title: Informationen zu Konvertierungs-Plug-ins
description: Informationen zu Konvertierungs-Plug-ins
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, Konvertierungs-Plug-ins
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Informationen
- Advanced Systems Format (ASF)
- ASF (Advanced Systems-Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708052"
---
# <a name="about-conversion-plug-ins"></a>Informationen zu Konvertierungs-Plug-ins

Sie können ein Windows Media Player-Plug-in erstellen, um digitale Mediendateien, die mithilfe von nicht von Microsoft bereitgestellten Technologien erstellt wurden, in das Advanced Systems Format (ASF) zu konvertieren.

Konvertierungs-Plug-ins sind Component Object Model (com)-Objekte, die als ausführbare Dateien (exe-Dateien) verpackt und verteilt werden. Windows Media Player instanziiert Konvertierungs-Plug-ins, um digitale Medienformate von Drittanbietern in den folgenden Szenarien zu konvertieren:

-   Der Inhalt digitaler Medien wird von einem tragbaren Gerät auf den Computer kopiert.
-   Inhalt digitaler Medien wird der Bibliothek mithilfe von **iwmpmediacollection:: Add** hinzugefügt.
-   Inhalt digitaler Medien wird mithilfe der Suchfunktion von Windows Media Player der Bibliothek hinzugefügt.
-   Inhalt digitaler Medien wird der Bibliothek von der Ordner Überwachungsfunktion von Windows Media Player hinzugefügt.
-   Inhalt digitaler Medien wird der Synchronisierungs Liste hinzugefügt, wenn der Benutzer eine Datei zieht und löscht.

Nachdem Windows Media Player eine Instanz eines Konvertierungs-Plug-Ins erstellt hat, muss das Plug-in die bereitgestellte Datei in ASF oder WMA konvertieren und relevante Metadaten hinzufügen. (Verwenden Sie nicht das Konvertierungs-Plug-in, um die Datei zu transcodieren.) Das Plug-in muss dann die konvertierte Datei in den angegebenen Ordner kopieren und den Pfad zur neuen Datei an Windows Media Player zurückgeben.

Konvertierungs-Plug-Ins müssen die **iwmpconvert** -Schnittstelle implementieren. Weitere Informationen finden Sie unter [Programmier Referenz für Konvertierungen](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Konvertierungsprozess**](about-the-conversion-process.md)
</dt> <dt>

[**Hinzufügen von Metadaten zu konvertierten Dateien**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Windows Media Player-Konvertierungs-Plug-ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




