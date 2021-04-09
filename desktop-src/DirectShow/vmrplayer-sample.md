---
description: Vmrplayer-Beispiel
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Vmrplayer-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863399"
---
# <a name="vmrplayer-sample"></a>Vmrplayer-Beispiel

## <a name="description"></a>BESCHREIBUNG

Dieses Beispiel verwendet den Filter Video Mischungs-Renderer 9 (VMR-9), um ein oder zwei laufende Videos und ein statisches Bild zu Alpha mischen.

## <a name="usage"></a>Verbrauch

Um das erste Video zu öffnen, wählen Sie im Menü **Datei** die Option **primären Stream öffnen** aus. Wenn Sie ein zweites Video öffnen möchten, wählen Sie im Menü **Datei** den Befehl **sekundären Stream öffnen** aus (Sie müssen zuerst den primären Stream öffnen). Um das Video wiederzugeben, klicken Sie auf die Schaltfläche wieder **Gabe** .

Sie können die Position, Größe und Alpha Werte der Videos festlegen, indem Sie im **VMR-Eigenschaften** Menü den **primären** oder den **sekundären Stream** auswählen.

Wenn Sie ein statisches Bitmap über das Video hinzufügen möchten, wählen Sie im **VMR-Eigenschaften** Menü die Option **static App Image** aus, und klicken Sie auf das Feld **App-Image** Sie können das gleiche Dialogfeld verwenden, um die Position, Größe und den Alpha Wert der Bitmap zu steuern.

Um das gemischte Video Bild zu erfassen, wählen Sie im **VMR-Eigenschaften** Menü die Option **Bitmapbild erfassen** aus.

Sie können den primären Bildstream auch über die Befehlszeile angeben:

**Vmrplayer** **/P** *Dateiname*

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



