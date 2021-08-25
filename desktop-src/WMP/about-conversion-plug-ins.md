---
title: Informationen zu Konvertierungs-Plug-Ins
description: Informationen zu Konvertierungs-Plug-Ins
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player,Konvertierungs-Plug-Ins
- Windows Media Player-Plug-Ins, Konvertierung
- Plug-Ins, Konvertierung
- Konvertierungs-Plug-Ins, Informationen
- Advanced Systems Format (ASF)
- ASF (Advanced Systems Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4331f2cc0cdf8726e2ba26e834c56546ee614e012a9dd6acdad56906d450b66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903550"
---
# <a name="about-conversion-plug-ins"></a>Informationen zu Konvertierungs-Plug-Ins

Sie können ein Windows Media Player Plug-In erstellen, um digitale Mediendateien, die mit technologien erstellt werden, die nicht von Microsoft bereitgestellt werden, in advanced Systems Format (ASF) zu konvertieren.

Konvertierungs-Plug-Ins sind COM-Objekte (Component Object Model), die als ausführbare Dateien (.exe) gepackt und verteilt werden. Windows Media Player instanziiert Konvertierungs-Plug-Ins, um digitale Medienformate von Drittanbietern in den folgenden Szenarien zu konvertieren:

-   Digitale Medieninhalte werden von einem portablen Gerät auf den Computer kopiert.
-   Digitale Medieninhalte werden der Bibliothek mithilfe von **IWMPMediaCollection::add** hinzugefügt.
-   Digitale Medieninhalte werden der Bibliothek mithilfe der Suchfunktion von Windows Media Player hinzugefügt.
-   Digitale Medieninhalte werden der Bibliothek durch die Ordnerüberwachungsfunktion von Windows Media Player hinzugefügt.
-   Digitale Medieninhalte werden der Synchronisierungsliste hinzugefügt, wenn der Benutzer eine Datei zieht und löscht.

Nachdem Windows Media Player eine Instanz eines Konvertierungs-Plug-Ins erstellt hat, muss das Plug-In die angegebene Datei in ASF oder WMA konvertieren und relevante Metadaten hinzufügen. (Verwenden Sie nicht das Konvertierungs-Plug-In, um die Datei zu transcodieren.) Das Plug-In muss dann die konvertierte Datei in den angegebenen Ordner kopieren und den Pfad zur neuen Datei zurückgeben, um Windows Media Player.

Konvertierungs-Plug-Ins müssen die **IWMPConvert-Schnittstelle** implementieren. Weitere Informationen finden Sie unter Programmierreferenz zu [Konvertierungs-Plug-Ins.](conversion-plug-ins-programming-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Konvertierungsprozess**](about-the-conversion-process.md)
</dt> <dt>

[**Hinzufügen von Metadaten zu konvertierten Dateien**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Windows Media Player Konvertierungs-Plug-Ins**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




