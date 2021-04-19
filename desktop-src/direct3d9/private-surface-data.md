---
description: Sie können beliebige Arten von anwendungsspezifischen Daten mit einer-Oberfläche speichern. Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen über das Gelände enthalten.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Private Oberflächendaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342971"
---
# <a name="private-surface-data-direct3d-9"></a>Private Oberflächendaten (Direct3D 9)

Sie können beliebige Arten von anwendungsspezifischen Daten mit einer-Oberfläche speichern. Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen über das Gelände enthalten.

Eine Oberfläche kann über mehr als einen privaten Datenpuffer verfügen. Jeder Puffer wird durch eine GUID identifiziert, die Sie angeben, wenn die Daten an die-Oberfläche angefügt werden.

Verwenden Sie zum Speichern privater Oberflächendaten setprivatedata, und übergeben Sie einen Zeiger auf den Quell Puffer, die Größe der Daten und eine von der Anwendung definierte GUID für die Daten. Optional können die Quelldaten in Form eines COM-Objekts vorhanden sein. in diesem Fall übergeben Sie einen Zeiger an den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Zeiger des Objekts und legen das Flag D3DSPD \_ iunknownpointer fest.

Setprivatedata ordnet einen internen Puffer für die Daten zu und kopiert ihn. Anschließend können Sie den Quell Puffer oder das Objekt sicher freigeben. Der interne Puffer-oder Schnittstellen Verweis wird freigegeben, wenn "freprivatedata" aufgerufen wird. Dies geschieht automatisch, wenn die Oberfläche freigegeben wird.

Zum Abrufen privater Daten für eine Oberfläche müssen Sie einen Puffer mit der richtigen Größe zuordnen und dann die getprivatedata-Methode aufrufen und dabei die GUID übergeben, die den Daten zugewiesen wurde. Sie sind dafür verantwortlich, den dynamischen Arbeitsspeicher freizugeben, den Sie für diesen Puffer verwenden. Wenn es sich bei den Daten um ein COM-Objekt handelt, ruft diese Methode den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger ab.

Wenn Sie nicht wissen, wie groß ein Puffer ist, müssen Sie zuerst getprivatedata mit 0 (null) in psizeofdata aufrufen. Wenn die Methode mit D3DERR \_ MoreData fehlschlägt, wird die erforderliche Anzahl von Bytes für den Puffer zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
