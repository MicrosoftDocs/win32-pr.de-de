---
description: 'Das Konzept des exklusiven Vollbildmodus wird in Direct3D 9 beibehalten, aber er wird in den Methoden aufrufen IDirect3D9:: kreatedevice und IDirect3DDevice9:: Reset vollständig implizit beibehalten.'
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Arbeiten mit mehreren Monitor Systemen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338858"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Arbeiten mit mehreren Monitor Systemen (Direct3D 9)

Das Konzept des exklusiven Vollbildmodus wird in Direct3D 9 beibehalten, aber er wird in den Methoden aufrufen [**IDirect3D9:: kreatedevice**](/windows/desktop/api) und [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) vollständig implizit beibehalten. Wenn ein Gerät erfolgreich zurückgesetzt oder im Vollbildmodus erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als Besitzer aller Adapter auf diesem System markiert. Dieser Status wird als exklusiver Modus bezeichnet, und an diesem Punkt besitzt das Direct3D-Objekt den exklusiven Modus. Der exklusive Modus bedeutet, dass Geräte, die von einem anderen von Direct3D9-Objekt erstellt werden, weder den voll Bild Vorgang annehmen noch Videospeicher zuordnen können. Wenn ein von Direct3D9-Objekt den exklusiven Modus annimmt, werden darüber hinaus alle anderen Geräte als das Gerät, das den Vollbildmodus aufging, in den verlorenen Zustand versetzt. Informationen zum behandeln verlorener Geräte finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).

Neben dem exklusiven Modus wird das von Direct3D9-Objekt über das Fokus Fenster informiert, das vom Gerät verwendet werden soll. Der exklusive Modus wird freigegeben, wenn das letzte voll Bild Gerät, das diesem von Direct3D9-Objekt gehört, entweder auf den Fenstermodus zurückgesetzt oder zerstört wird.

Geräte können in zwei Kategorien unterteilt werden, wenn ein von Direct3D9-Objekt im exklusiven Modus ist. Die erste Kategorie von Geräten sind solche, die vom gleichen von Direct3D9-Objekt erstellt wurden, das das bereits voll Bild geschützte Gerät erstellt hat, das gleiche Fokus Fenster wie das bereits vollständige Bildschirm hat und einen anderen Adapter als ein beliebiges voll Bild Gerät darstellt. Geräte in dieser Kategorie haben keine Einschränkungen hinsichtlich ihrer Fähigkeit, zurückgesetzt oder erstellt zu werden, und werden nicht in den verlorenen Zustand versetzt. Geräte in dieser Kategorie können sogar in den Vollbildmodus versetzt werden.

Geräte, die nicht in dieser Kategorie vorhanden sind, die von einem anderen von Direct3D9-Objekt oder mit einem anderen Fokus Fenster erstellt werden, oder für einen Adapter mit einem bereits vollständigen Gerät können nicht zurückgesetzt werden und bleiben im verlorenen Zustand, bis der exklusive Modus verloren geht.

Die praktische Implikation besteht darin, dass eine Anwendung mit mehreren Monitoren mehrere Geräte im Vollbildmodus platzieren kann, aber nur, wenn alle diese Geräte für verschiedene Adapter vorhanden sind, die vom gleichen von Direct3D9-Objekt erstellt wurden und alle das gleiche Fokus Fenster verwenden.

Wenn Sie ein neues Gerät mit dem gleichen [**IDirect3D9**](/windows/desktop/api) -Objekt und dem gleichen Fokus Fenster erstellen, verliert ihr ursprüngliches Gerät seine Oberflächen. Sie müssen [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) auf dem ersten Gerät anrufen, damit Sie von Ihrer Anwendung verwendet werden kann. Gehen Sie beispielsweise wie folgt vor, um zwei Geräte zu erstellen:

1.  Erstellen von Gerät 1
2.  Erstellen von Gerät 2
3.  Gerät zurücksetzen 1

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
