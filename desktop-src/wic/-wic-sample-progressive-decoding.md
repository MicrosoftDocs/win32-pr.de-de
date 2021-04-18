---
description: Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren eines Bilds, das mit progressiven Ebenen codiert ist.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Beispiel für eine progressive WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106365362"
---
# <a name="wic-progressive-decoding-sample"></a>Beispiel für eine progressive WIC

Dieses Beispiel veranschaulicht die Verwendung der Windows Imaging Component (WIC) zum Decodieren eines Bilds, das mit progressiven Ebenen codiert ist. In diesem Beispiel wird Direct2D verwendet, um die verschiedenen progressiven Ebenen auf dem Bildschirm zu erzeugen.

## <a name="requirements"></a>Anforderungen

Für dieses Beispiel gelten die folgenden Anforderungen:

| Anforderung | Wert |
|-|
| Unterstützte Mindestversion (Client) | Windows 7 |
| Minimale Windows SDK | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für Windows 7 |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist für die [Progressive WIC-Codierung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding)verfügbar.

## <a name="building-the-sample"></a>Erstellen des Beispiels

### <a name="using-visual-studio-preferred-method"></a>Verwenden von Visual Studio (bevorzugte Methode)

1. Öffnen Sie Windows Explorer, und navigieren Sie zum Verzeichnis.
2. Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um die Datei in Visual Studio zu öffnen.
3. Wählen Sie im Menü Erstellen die Option Projektmappe erstellen aus. Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.

### <a name="using-the-command-prompt"></a>Verwenden der Eingabeaufforderung

So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung

1. Öffnen Sie die Eingabeaufforderung, und navigieren Sie zum Beispiel Verzeichnis.
2. Geben Sie `msbuild WICProgressiveDecoding.sln` ein

## <a name="running-the-sample"></a>Ausführen des Beispiels

Nachdem die Anwendung gestartet wurde, laden Sie eine Bilddatei über das Menü Datei öffnen. Beim Laden wird die standardmäßige Progressive Ebene auf 0 festgelegt. Sie können entweder über das Menü oder die nach-unten-Taste zu verschiedenen progressiven Ebenen navigieren. Der aktuelle Text der progressiven Ebene wird in der Statusleiste des Hauptfensters angezeigt. Die Fenstergröße wird unterstützt.

> [!NOTE]
> Die Progressive Decodierung ist nur für Images verfügbar, die progressiv codiert wurden. Das in diesem Beispiel bereitgestellte Image wurde progressiv codiert.

## <a name="see-also"></a>Siehe auch

[Microsoft Windows Imaging-Codec](-wic-lh.md)

[Programmier Handbuch](-wic-programming-guide.md)

[Verweis](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Beispiele und Codebeispiele](-wic-samples.md)

[Übersicht über Progressive Decodierung](-wic-progressive-decoding.md)
