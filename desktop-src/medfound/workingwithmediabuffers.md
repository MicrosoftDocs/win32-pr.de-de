---
description: Arbeiten mit DMO Medienpuffern
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Arbeiten mit DMO Medienpuffern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311778898fbfa669a602cd189fb5518f7a2814089a87ed33fba7e303c4327cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236956"
---
# <a name="working-with-dmo-media-buffers"></a>Arbeiten mit DMO Medienpuffern

Eingabedaten werden mithilfe von Medienpuffern an die Codec-DMOs übergeben. Ein Medienpuffer ist ein Objekt, das die [**IMediaBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementiert. Sie können zu diesem Zweck eine Klasse implementieren. Wenn Sie das Windows Media Format SDK in Ihrer Anwendung verwenden, können Sie die Pufferobjekte verwenden, die in diesem SDK definiert sind.

Wenn Sie Ihre eigene Pufferklasse implementieren, sollten Sie darauf achten, wie der Pufferspeicher behandelt wird. Wenn Sie ein Eingabebeispiel übergeben, behält der DMO einen Verweis auf den Puffer bei, bis er mit dem Beispiel fertig ist. Sie können Ihren Verweis sofort auf die [**IMediaBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) freigeben, aber Sie können nicht wissen, wann der Codec seinen Verweis nicht mehr benötigt. Um sicherzugehen, dass der Arbeitsspeicher freigegeben wird, wenn das Objekt sich selbst löscht, sollten Sie Ihre -Klasse implementieren, damit sie den Arbeitsspeicher für den Puffer intern zuordnet und freigibt.

Da die DMOs für einen unbekannten Zeitraum Verweise auf Puffer beibehalten, ist es keine triviale Aufgabe, einen begrenzten Pool von Puffern zu verwenden. Die einfachste Lösung besteht darin, für jede Stichprobe einen neuen Puffer zuzuordnen, obwohl dies ineffizient ist.

Eine bessere Lösung besteht darin, ein Objekt zum Verwalten eines Pufferpools zu implementieren. Schreiben Sie hierzu Code in die **Release-Methode** Ihrer [**IMediaBuffer-Implementierung,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) der eine Methode Ihres Puffer-Managers aufruft (anstatt sich selbst zu löschen), wenn der Verweiszähler auf null fällt. Der Puffer-Manager kann dann eine Liste von Zeigern auf zugeordnete Pufferobjekte verwalten. Erstellen Sie eine Methode in Ihrem Puffer-Manager, um die Liste der freien Puffer zu überprüfen und einen Zeiger zurückzugeben, damit Ihre Anwendung bei Bedarf auf Puffer zugreifen kann. Diese Methode sollte bei Bedarf neue Puffer erstellen und der Liste hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
