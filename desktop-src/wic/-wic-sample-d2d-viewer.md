---
description: Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren einer Bilddatei und Direct2D, um das Bild auf dem Bildschirm zu Rendering.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: WIC-Image-Viewer mit Direct2D-Beispiel
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106364023"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>WIC-Image-Viewer mit Direct2D-Beispiel

Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren einer Bilddatei und Direct2D, um das Bild auf dem Bildschirm zu Rendering.

## <a name="requirements"></a>Anforderungen

Für dieses Beispiel gelten die folgenden Anforderungen:

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows Vista |
| Minimale Windows SDK | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7 |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [WIC-Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d)verfügbar.

## <a name="building-the-sample"></a>Erstellen des Beispiels

### <a name="using-visual-studio-preferred-method"></a>Verwenden von Visual Studio (bevorzugte Methode)

1. Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.
2. Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.
3. Wählen Sie im Menü **Erstellen** die Option **Projektmappe erstellen** aus. Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.

### <a name="using-the-command-prompt"></a>Verwenden der Eingabeaufforderung

So erstellen Sie das Beispiel mithilfe einer Eingabeaufforderung:

1. Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zum Beispiel Verzeichnis.
2. Geben Sie `msbuild WICViewerD2D.sln` ein

## <a name="running-the-sample"></a>Ausführen des Beispiels

Nachdem Sie die Anwendung gestartet haben, laden Sie eine Bilddatei mit dem Befehl **Öffnen** im Menü **Datei** .

## <a name="see-also"></a>Siehe auch

[Microsoft Windows Imaging-Codec](-wic-lh.md)

[Programmier Handbuch](-wic-programming-guide.md)

[Verweis](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Beispiele und Codebeispiele](-wic-samples.md)
