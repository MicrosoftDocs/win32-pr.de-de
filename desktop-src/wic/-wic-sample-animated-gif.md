---
description: Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen der entsprechenden Metadaten für jeden Frame, das Zusammenstellen von Frames und das Rendern der Animation mit Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Animiertes GIF-Beispiel für WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 925beb45b58bdecb7d12505a9d2067cbcb9e6fbf1867786286f18333fea986e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709600"
---
# <a name="wic-animated-gif-sample"></a>Animiertes GIF-Beispiel für WIC

Dieses Beispiel veranschaulicht das Decodieren verschiedener Frames in einer GIF-Datei, das Lesen der entsprechenden Metadaten für jeden Frame, das Zusammenstellen von Frames und das Rendern der Animation mit Direct2D.

## <a name="requirements"></a>Anforderungen

Für dieses Beispiel gelten die folgenden Anforderungen.

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 7 |
| Minimum Windows SDK | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7 |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist unter AnimierteS [GIF von WIC verfügbar.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)

## <a name="building-the-sample"></a>Erstellen des Beispiels

### <a name="using-visual-studio-preferred-method"></a>Verwenden Visual Studio (bevorzugte Methode)

1. Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.
2. Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappe), um die Datei im Visual Studio.
3. Wählen Sie im Menü **Erstellen** die Option **Projektmappe erstellen** aus. Die Anwendung wird im Standardverzeichnis \\ Debuggen oder \\ Release erstellt.

### <a name="using-the-command-prompt"></a>Verwenden der Eingabeaufforderung

So erstellen Sie das Beispiel mithilfe einer Eingabeaufforderung.

1. Öffnen Sie die Eingabeaufforderung, und navigieren Sie zum Beispielverzeichnis.
2. Geben Sie `msbuild WICAnimatedGif.sln` ein

## <a name="running-the-sample"></a>Ausführen des Beispiels

Laden Sie nach dem Start der Anwendung eine Bilddatei mithilfe des Befehls **Öffnen** im **Menü Datei.** Die Größenver ändern des Fensters wird unterstützt.

## <a name="see-also"></a>Siehe auch

[Microsoft Windows Imaging Codec](-wic-lh.md)

[Programmierhandbuch](-wic-programming-guide.md)

[Referenz](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Beispiele und Codebeispiele](-wic-samples.md)
