---
title: Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern
description: Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- Mciwndgetsource-Makro
- Mciwndputsource-Makro
- Mciwndgetdest-Makro
- Mciwndputdest-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724809"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Bereitstellen von Steuerelementen zum Zuschneiden und Strecken von Bildern

Mit mciwnd können Sie Bilder eines Videoclips Zuschneiden und Strecken. Um diese Features zu verstehen, müssen Sie die Beziehungen zwischen *Frame Größe*, *Quell Rechteck*, *Ziel Rechteck* und *Wiedergabe Bereich* verstehen.

Ein Videoclip besteht aus mehreren Frames, die jeweils ein Bild enthalten. Die Rahmengröße eines Videoclips ist die Größe des Bilds im aktuellen Frame. In der Regel hat ein Videoclip eine Frame Größe, da alle Bilder im Clip die gleiche Größe haben.

Das Quell Rechteck ist ein rechteckiger Bereich, der die Frames eines Videoclips überlagert. Das Quell Rechteck definiert den Teil jedes Frames, der während der Wiedergabe angezeigt wird. Wenn ein Videoclip mit mciwnd geladen wird, wird das Quell Rechteck mit denselben Dimensionen und der gleichen Position wie der erste Frame des Videoclips initialisiert.

Das Ziel Rechteck ist ein rechteckiger Bereich, der ein virtuelles Wiedergabe Fenster definiert. Das Ziel Rechteck empfängt die Bilddaten aus dem Quell Rechteck für jeden Frame des Videoclips. Wenn die Größe des Quell-und Ziel Rechtecks unterschiedlich ist, passt mciwnd die Bilddaten bei Bedarf horizontal und vertikal an, um das Ziel Rechteck auszufüllen. Wenn ein Videoclip mit mciwnd geladen wird, wird das Ziel Rechteck mit denselben Dimensionen und der gleichen Position wie der erste Frame des Videoclips initialisiert.

Der Wiedergabe Bereich ist der Teil eines mciwnd-Fensters, den eine Anwendung verwendet, um den Videoclip anzuzeigen. Der Wiedergabe Bereich ist der Client Bereich eines mciwnd-Fensters oder der Teil des Client Bereichs, von dem die mciwnd-Symbolleiste ausgeschlossen wird. Wenn ein Videoclip mit mciwnd geladen wird, wird der Wiedergabe Bereich mit denselben Dimensionen und der gleichen Position wie der erste Frame des Videoclips initialisiert.

Sie können einen Videoclip mit den Makros " [**mciwndgetsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) " und " [**mciwndputsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) " zum Ändern des Quell Rechtecks zuschneiden. Beim Zuschneiden eines Bilds wird nur bestimmt, welcher Teil der Rahmen während der Wiedergabe angezeigt wird. der Inhalt der wiedergegebenen Datei wird nicht geändert. Bevor Sie ein Bild zuschneiden, können Sie die aktuelle Größe des Quell Rechtecks mithilfe von **mciwndgetsource** abrufen. Nachdem Sie die neue Größe und Position des Quell Rechtecks berechnet haben, können Sie die zuschnittgrenzen des Quell Rechtecks mithilfe von " **mciwndputsource**" festlegen.

Sie können einen Videoclip mithilfe der Makros [**mciwndgetdest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) und [**mciwndputdest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) Strecken, um das Ziel Rechteck zu ändern. Wenn Sie einen Videoclip Strecken, verlängern Sie die Frame Größe eines Videoclips vertikal, horizontal oder in beide Richtungen. Vor dem Strecken eines Bilds können Sie die aktuelle Größe und Position des Ziel Rechtecks mithilfe von **mciwndgetdest** abrufen. Mit dem **mciwndputdest** -Makro können Sie das Ziel Rechteck neu definieren. Durch das Stretching kann das Bild während der Wiedergabe verzerrt werden, aber der Inhalt der wiedergegebenen Datei wird nicht geändert.

Wenn die Größe des Ziel Rechtecks größer als der Wiedergabe Bereich ist, können Sie angeben, welcher Teil des Wiedergabe Bereichs den Videoclip mithilfe von " **mciwndputdest**" anzeigt.

> [!Note]  
> Das [**mciwndputdest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) -Makro ändert nicht die Größe des Wiedergabe Bereichs. Um das mciwnd-Fenster zusammen mit dem Ziel Rechteck zu Strecken, müssen Sie die aktuelle Größe des mciwnd-Fensters kennen und neue Fenster Dimensionen auf der Grundlage des Ziel Rechtecks ausgeben. Sie können die mciwnd-Fenster Dimensionen mithilfe der [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) -Funktion abrufen und die Größe des mciwnd-Fensters ändern, indem Sie die [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) -Funktion verwenden.

 

 

 