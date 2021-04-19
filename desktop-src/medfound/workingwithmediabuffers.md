---
description: Arbeiten mit DMO-Medien Puffern
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Arbeiten mit DMO-Medien Puffern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353254"
---
# <a name="working-with-dmo-media-buffers"></a>Arbeiten mit DMO-Medien Puffern

Eingabedaten werden mithilfe von Medien Puffern an die Codec-DMOS übermittelt. Ein Medien Puffer ist ein Objekt, das die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle implementiert. Zu diesem Zweck können Sie eine Klasse implementieren, oder Sie können die Puffer Objekte verwenden, die in diesem SDK definiert sind, wenn Sie das Windows Media-Format-SDK in der Anwendung verwenden.

Wenn Sie Ihre eigene Puffer Klasse implementieren, achten Sie darauf, wie der Puffer Arbeitsspeicher verarbeitet wird. Wenn Sie ein Eingabe Beispiel übergeben, behält der DMO einen Verweis auf den Puffer bei, bis das Beispiel abgeschlossen ist. Sie können den Verweis auf die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle sofort freigeben, aber Sie können nicht wissen, wann der Codec seinen Verweis nicht mehr benötigt. Um sicherzustellen, dass der Arbeitsspeicher freigegeben wird, wenn das Objekt sich selbst löscht, sollten Sie die Klasse implementieren, damit Sie den Speicher für den Puffer intern zuordnet und freigibt.

Da der DMOS für einen unbekannten Zeitraum Verweise auf Puffer aufbewahrt, ist es nicht sehr wichtig, einen begrenzten Pufferpool zu verwenden. Die einfachste Lösung besteht darin, für jedes Beispiel einen neuen Puffer zuzuweisen, obwohl dies ineffizient ist.

Eine bessere Lösung ist die Implementierung eines Objekts zum Verwalten eines Pufferpools. Schreiben Sie hierzu Code in der **releasemethode** Ihrer [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Implementierung, die eine Methode Ihres Puffer-Managers aufruft (anstatt sich selbst zu löschen), wenn der Verweis Zähler auf 0 (null) sinkt. Der Puffer-Manager kann dann eine Liste von Zeigern auf zugewiesene Puffer Objekte warten. Erstellen Sie im Puffer-Manager eine Methode, um die Liste der freien Puffer zu überprüfen und einen Zeiger zurückzugeben, damit Ihre Anwendung bei Bedarf auf Puffer zugreifen kann. Diese Methode sollte bei Bedarf neue Puffer erstellen und Sie der Liste hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
