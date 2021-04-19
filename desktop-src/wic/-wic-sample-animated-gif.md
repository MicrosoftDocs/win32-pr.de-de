---
description: Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen entsprechender Metadaten für jeden Frame, das Verfassen von Frames und das Rendern der Animation mit Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: WIC animieren GIF-Beispiel
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353412"
---
# <a name="wic-animated-gif-sample"></a>WIC animieren GIF-Beispiel

Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen entsprechender Metadaten für jeden Frame, das Verfassen von Frames und das Rendern der Animation mit Direct2D.

## <a name="requirements"></a>Anforderungen

Für dieses Beispiel gelten die folgenden Anforderungen:

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 7 |
| Minimale Windows SDK | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7 |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel finden Sie unter [WIC animierte GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).

## <a name="building-the-sample"></a>Erstellen des Beispiels

### <a name="using-visual-studio-preferred-method"></a>Verwenden von Visual Studio (bevorzugte Methode)

1. Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.
2. Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.
3. Wählen Sie im Menü **Erstellen** die Option **Projektmappe erstellen** aus. Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.

### <a name="using-the-command-prompt"></a>Verwenden der Eingabeaufforderung

So erstellen Sie das Beispiel mithilfe einer Eingabeaufforderung

1. Öffnen Sie die Eingabeaufforderung, und navigieren Sie zum Beispiel Verzeichnis.
2. Geben Sie `msbuild WICAnimatedGif.sln` ein

## <a name="running-the-sample"></a>Ausführen des Beispiels

Nachdem die Anwendung gestartet wurde, laden Sie eine Bilddatei mit dem Befehl **Öffnen** im Menü **Datei** . Die Fenstergröße wird unterstützt.

## <a name="see-also"></a>Siehe auch

[Microsoft Windows Imaging-Codec](-wic-lh.md)

[Programmier Handbuch](-wic-programming-guide.md)

[Verweis](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Beispiele und Codebeispiele](-wic-samples.md)
