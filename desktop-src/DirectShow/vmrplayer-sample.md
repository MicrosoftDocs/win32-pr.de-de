---
description: VMRPlayer-Beispiel
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: VMRPlayer-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6281147e2c140541ade480e5b2a5e0f0a1d4146dde59b4871441b68fec6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071914"
---
# <a name="vmrplayer-sample"></a>VMRPlayer-Beispiel

## <a name="description"></a>Beschreibung

In diesem Beispiel wird der Filter Video Mixing Renderer 9 (VMR-9) verwendet, um ein oder zwei ausgeführte Videos und ein statisches Bild alphaneinzublenden.

## <a name="usage"></a>Verwendung

Um das erste Video zu öffnen, wählen Sie im Menü **Datei** die Option **Primären Stream öffnen** aus. Um ein zweites Video zu öffnen, wählen Sie im Menü **Datei** die Option **Sekundären Stream** öffnen aus (Sie müssen zuerst den primären Stream öffnen). Um das Video wiederzuspielen, klicken Sie auf die Schaltfläche **Wiedergeben.**

Sie können die Position, Größe und Alphawerte der Videos festlegen, indem Sie im **VmR-Eigenschaftenmenü** **Primary Stream** oder **Secondard Stream** auswählen.

Um eine statische Bitmap über dem Video hinzuzufügen, wählen Sie **statisches App-Image** aus dem **VMR-Eigenschaftenmenü** aus, und klicken Sie auf das Feld **App-Image anzeigen.** Sie können dasselbe Dialogfeld verwenden, um position, size und alpha value der Bitmap zu steuern.

Wählen Sie zum Erfassen des gemischten Videobilds im **VMR-Menü Eigenschaften** die Option **Bitmapbild erfassen** aus.

Sie können den primären Imagestream auch über die Befehlszeile angeben:

**VMRPlayer** **/P** *filename*

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



