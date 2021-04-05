---
title: Dateneinheiten Erweiterungen
description: Dateneinheiten Erweiterungen
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media-Format-SDK, Dateneinheiten Erweiterungen
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Windows Media-Format-SDK, Nutz Last Erweiterungs Systeme
- Advanced Systems Format (ASF), Nutz Last Erweiterungs Systeme
- ASF (Advanced Systems Format), Nutz Last Erweiterungs Systeme
- Dateneinheiten Erweiterungen, Informationen zu
- Nutz Last Einheiten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723496"
---
# <a name="data-unit-extensions"></a>Dateneinheiten Erweiterungen

Mit dem Windows Media-Format-SDK können Sie Daten in Beispielen mit *Dateneinheiten Erweiterungen* ergänzen, die auch als Nutz Last Erweiterungs Systeme bezeichnet werden. In dieser Dokumentation wird der Begriff "Dateneinheiten Erweiterungen" verwendet, damit Sie mit Methodennamen wie [**adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)konsistent bleiben. Eine Dateneinheiten Erweiterung ist ein Name-Wert-Paar, das im Daten Abschnitt der Datei an das Beispiel angefügt wird. Sie können auf die erweiterten Daten mithilfe der Methoden des Buffer-Objekts zugreifen, wenn das Beispiel vom Reader abgerufen wird.

Sie können Dateneinheiten Erweiterungen für Ihre eigenen Spezifikationen erstellen, aber mehrere Typen sind vordefiniert und werden von den Objekten dieses SDK unterstützt. Diese Standard Erweiterungen werden verwendet, um zusätzliche Daten für Dateinamen (in Skript-und Webstreams), SMPTE-Zeit Code Daten, ein nicht quadratisches Pixel-Seitenverhältnis, eine Dauer und einen Typ von Interlacing bereitzustellen.

Um dateneinheits Erweiterungen zu verwenden, müssen Sie den Stream so konfigurieren, dass Sie akzeptiert werden, und dann den einzelnen Beispielen für diesen Stream Erweiterungen hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Konfigurieren von Dateneinheitserweiterung en**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Festlegen von Dateneinheiten Erweiterungen**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




