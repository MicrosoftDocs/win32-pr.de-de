---
title: Informationen zum Konvertierungsprozess
description: Informationen zum Konvertierungsprozess
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, Konvertierungsprozess
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038573"
---
# <a name="about-the-conversion-process"></a>Informationen zum Konvertierungsprozess

Nachdem das Konvertierungs-Plug-in von Windows Media Player instanziiert wurde, wird der Prozess wie folgt fortgesetzt:

1.  Der Player ruft [iwmpconvert:: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile)auf.
2.  Das Plug-in konvertiert die im *bstrinputfile* -Parameter bereitgestellte Datei in ein ASF-Format.
3.  Wenn die Konvertierung aus irgendeinem Grund fehlschlägt, gibt das Plug-in einen entsprechenden Fehlercode zurück, und der Prozess wird beendet.
4.  Wenn die Konvertierung erfolgreich ist, platziert das Plug-in die konvertierte Datei in dem Ordner, der im Parameter *bstrodestinationfolder* bereitgestellt wird, und gibt den voll qualifizierten Pfad zur konvertierten Datei über den *pbstroutputfile* -Parameter zurück.
5.  Das Plug-in gibt einen Erfolgs Code aus **convertfile** zurück.
6.  Der Player kopiert die konvertierte Datei in einen Ordner in der Musik Ordnerhierarchie des Benutzers. Genau, wo der Player die Datei kopiert, hängt vom Inhalt ab. Im Rahmen dieses Prozesses kann der Spieler die Datei umbenennen.
7.  Der Player kopiert die ursprüngliche (nicht konvertierte) Datei in einen Ordner in der Musik Ordnerhierarchie des Benutzers. Im Rahmen dieses Prozesses kann der Spieler die Datei umbenennen. Dies ist die Kopie der Datei, die der Player verwendet, wenn der Benutzer den Inhalt des Computers mit einem Gerät synchronisiert, das das ursprüngliche Dateiformat erfordert. Diese Datei wird als *Schattendatei* bezeichnet.
8.  Der-Player Fügt der Bibliothek Informationen zur konvertierten Datei hinzu. Dies schließt das Festlegen des Werts für das **shadowfilepath** -Attribut auf den neuen Speicherort ein, an dem die Schattendatei gespeichert wird.

Wenn Sie mit der konvertierten Datei arbeiten müssen, können Sie die Bibliothek Abfragen, um den Inhalt mithilfe der Attribute **contentdistributor** und **WM/UniqueFileIdentifier** abzurufen. Wenn Sie mit der Schattendatei arbeiten müssen, müssen Sie dennoch das **Medien** Objekt für die konvertierte Datei abrufen und dann das **shadowfilepath** -Attribut Abfragen. Siehe [Hinzufügen von Metadaten zu konvertierten Dateien](adding-metadata-to-converted-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Konvertierungs-Plug-ins**](about-conversion-plug-ins.md)
</dt> <dt>

[**Hinzufügen von Metadaten zu konvertierten Dateien**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Shadowfilepath-Attribut**](shadowfilepath-attribute.md)
</dt> <dt>

[**WM-/contentverteilungs-Attribut**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**WM/UniqueFileIdentifier-Attribut**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




