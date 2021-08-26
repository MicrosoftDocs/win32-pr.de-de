---
title: Art Files
description: Art Files
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player Skins, Art-Dateien
- Skins, Art-Dateien
- Dateien für Skins, Art
- Grafikdateien für Skins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ccf07757e511f7717cbe3bbeff2cdacee004da8d3b64d27ddcef7ae2199a29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956370"
---
# <a name="art-files"></a>Art Files

Sie müssen eine oder mehrere Grafikdateien für Ihre Skin erstellen. Ohne Dies ist für den Benutzer nichts zu sehen. Sie könnten eine unsichtbare Skin erstellen, aber niemand würde sie sehen! Und selbst dann müssten Sie immer noch Grafikdateien erstellen, um Ihre unsichtbaren Bilder zu speichern, da die Skindefinitionsdatei Für bestimmte Elemente Grafikdateien benötigt.

Es gibt drei Verwendungsmöglichkeiten für Grafiken in Skins: primäre Bilder, Zuordnungsbilder und alternative Bilder.

## <a name="primary-images"></a>Primäre Images

Sie müssen ein primäres Image für Ihre Skin erstellen. Dies wird den Benutzern angezeigt, wenn sie Ihre Skin installieren. Das primäre Bild besteht aus einem oder mehreren Bildern, die von bestimmten Skinsteuerelementen erstellt werden.

Wenn Sie über mehrere Steuerelemente verfügen, müssen Sie die Z-Reihenfolge angeben, die definiert, welche Steuerelemente vor anderen Steuerelementen angezeigt werden. Jedes **View-Element** hat ein Hintergrundbild, dem Sie weitere Elementbilder hinzufügen können, sodass Sie ein primäres zusammengesetztes Bild erstellen können.

Möglicherweise verfügen Sie auch über sekundäre Bilder, z. B. eine Schiebeleiste, die nicht angezeigt werden, wenn Ihre Skin zum ersten Mal angezeigt wird, die jedoch angezeigt werden, wenn der Benutzer maßnahmen. Diese folgen den gleichen Regeln wie primäre Images, da sie mit einer Reihe von Steuerelementen erstellt werden.

## <a name="mapping-images"></a>Zuordnen von Bildern

Eines der leistungsstärksten Features von Windows Media Player Skins ist die Verwendung der Bildzuordnung, um Ereignisse für Ihre Skin auszulösen. Bildzuordnungen sind Dateien, die spezielle Bilder enthalten. Die Bilder in einer Bildzuordnungsdatei sind jedoch nicht für die Anzeige durch den Benutzer vorgesehen, sondern werden von Windows Media Player verwendet, um Maßnahmen zu ergreifen, wenn der Benutzer auf Ihre Skin klickt.

Verschiedene Steuerelemente benötigen unterschiedliche Arten von Bildzuordnungen. Wenn Sie z. B. einen Teil einer Bildkarte mit einem bestimmten roten Wert farbieren und der Benutzer auf den entsprechenden Bereich Ihres primären Bilds klickt, löst eine Schaltfläche ein Ereignis aus. Farbe wird verwendet, um zu definieren, welche Ereignisse ausgelöst werden, indem in einem bestimmten Bereich der Skin geklickt wird.

## <a name="alternate-images"></a>Alternative Bilder

Sie können auch alternative Bilder einrichten, die angezeigt werden, wenn ein Benutzer etwas tut. Beispielsweise können Sie ein alternatives Bild einer Schaltfläche erstellen, das nur angezeigt wird, wenn der Mauszeiger auf die Schaltfläche zeigt. Dies ist eine gute Möglichkeit, Benutzer darüber zu informieren, was sie tun können, und ermöglicht auch eine hochgradig erkennbare Benutzeroberfläche. Wenn Sie QuickInfos verwenden und mit dem Mauszeiger auf Bilder zeigen, können Sie ungewöhnliche Benutzeroberflächen erstellen, die dem Benutzer weiterhin Feedback zu den verfügbaren Optionen geben.

Die folgenden Abschnitte enthalten weitere Informationen zu Grafikdateien:

-   [Primäre Images](primary-images.md)
-   [Zuordnen von Bildern](mapping-images.md)
-   [Alternative Bilder](alternate-images.md)
-   [Art-Dateiformate](art-file-formats.md)
-   [Beispiel für einfaches Art](simple-art-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skindateien**](skin-files.md)
</dt> </dl>

 

 




