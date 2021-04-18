---
title: Kunstdateien
description: Kunstdateien
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338411"
---
# <a name="art-files"></a>Kunstdateien

Sie müssen eine oder mehrere kunstdateien für Ihre Skin erstellen. Ohne Kunst kann der Benutzer nichts überprüfen. Sie könnten ein unsichtbares Skin erstellen, aber niemand würde es sehen. Selbst dann müssten Sie trotzdem kunstdateien für ihre unsichtbaren Bilder erstellen, da die Skin-Definitionsdatei kunstdateien für bestimmte Elemente erfordert.

Es gibt drei Verwendungsmöglichkeiten für Kunst in Skins: primäre Bilder, Mapping-Bilder und alternative Bilder.

## <a name="primary-images"></a>Primäre Images

Sie müssen ein primäres Image für Ihre Skin erstellen. Dies wird den Benutzern angezeigt, wenn Sie Ihre Skin installieren. Das primäre Image besteht aus einem oder mehreren Bildern, die von bestimmten Skin-Steuerelementen erstellt werden.

Wenn Sie über mehr als ein Steuerelement verfügen, müssen Sie die z-Reihenfolge angeben, mit der definiert wird, welche Steuerelemente vor anderen Steuerelementen angezeigt werden. Jedes **Ansichts** Element verfügt über ein Hintergrundbild, dem Sie andere Element Bilder hinzufügen können, sodass Sie ein primäres verbundbild erstellen können.

Möglicherweise verfügen Sie auch über sekundäre Images, z. b. eine gleitende Leiste, die nicht angezeigt wird, wenn die Skin zum ersten Mal angezeigt wird. Diese werden jedoch angezeigt, wenn der Benutzer eine Aktion durchführt. Diese Regeln folgen denselben Regeln wie primäre Images, da Sie mit einem Satz von Steuerelementen erstellt werden.

## <a name="mapping-images"></a>Mapping von Bildern

Eines der leistungsstärksten Features von Windows Media Player Skins ist, dass Sie die Image Zuordnung verwenden können, um Ereignisse für Ihre Skin zu Triggern zu verwenden. Bild Zuordnungen sind Dateien, die besondere Bilder enthalten. Die Bilder in einer Imagemapdatei sind jedoch nicht zum Anzeigen durch den Benutzer gedacht, sondern werden von Windows Media Player verwendet, um Maßnahmen zu ergreifen, wenn der Benutzer auf die Skin klickt.

Für verschiedene Steuerelemente sind unterschiedliche Arten von Bild Zuordnungen erforderlich. Wenn Sie z. b. einem Teil eines Bilds einen bestimmten roten Wert zuordnen und der Benutzer auf den entsprechenden Bereich des primären Bilds klickt, wird ein Ereignis durch eine Schaltfläche ausgelöst. Die Farbe wird verwendet, um zu definieren, welche Ereignisse ausgelöst werden, indem Sie auf einen bestimmten Bereich der Skin klicken.

## <a name="alternate-images"></a>Alternative Images

Sie können auch alternative Images einrichten, die angezeigt werden, wenn ein Benutzer etwas bewirkt. Beispielsweise können Sie ein alternatives Bild einer Schaltfläche erstellen, das nur angezeigt wird, wenn mit dem Mauszeiger auf die Schaltfläche gezeigt wird. Dies ist eine gute Möglichkeit, den Benutzern mitzuteilen, was Sie tun können, und es ist auch möglich, eine stark erkennbare Benutzeroberfläche zu verwenden. Durch die sorgfältige Verwendung von Quick Infos und Hover-Bildern können Sie ungewöhnliche Benutzeroberflächen erstellen, die dem Benutzer weiterhin Feedback zu den verfügbaren Optionen geben.

In den folgenden Abschnitten finden Sie weitere Informationen zu kunstdateien:

-   [Primäre Images](primary-images.md)
-   [Mapping von Bildern](mapping-images.md)
-   [Alternative Images](alternate-images.md)
-   [Kunst Dateiformate](art-file-formats.md)
-   [Beispiel für einfache Kunst](simple-art-example.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Dateien**](skin-files.md)
</dt> </dl>

 

 




