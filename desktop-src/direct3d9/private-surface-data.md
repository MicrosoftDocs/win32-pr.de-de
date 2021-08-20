---
description: Sie können jede Art von anwendungsspezifischen Daten mit einer Oberfläche speichern. Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen zum Gelände enthalten.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Private Surface-Daten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c010e24f691dc64c75e4dcea428af21d46ebfcb95b31775b9c8db81b2263e6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520192"
---
# <a name="private-surface-data-direct3d-9"></a>Private Surface-Daten (Direct3D 9)

Sie können jede Art von anwendungsspezifischen Daten mit einer Oberfläche speichern. Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen zum Gelände enthalten.

Eine Oberfläche kann mehrere private Datenpuffer enthalten. Jeder Puffer wird durch eine GUID identifiziert, die Sie beim Anfügen der Daten an die Oberfläche bereitstellen.

Verwenden Sie zum Speichern privater Oberflächendaten SetPrivateData, indem Sie einen Zeiger auf den Quellpuffer, die Größe der Daten und eine anwendungsdefinierte GUID für die Daten übergeben. Optional können die Quelldaten in Form eines COM-Objekts vorhanden sein. In diesem Fall übergeben Sie einen Zeiger auf den [**IUnknown-Schnittstellenzeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Objekts und legen das Flag D3DSPD \_ IUNKNOWNPOINTER fest.

SetPrivateData ordnet einen internen Puffer für die Daten zu und kopiert sie. Anschließend können Sie den Quellpuffer oder das Quellobjekt sicher freigeben. Der interne Puffer- oder Schnittstellenverweis wird freigegeben, wenn FreePrivateData aufgerufen wird. Dies geschieht automatisch, wenn die Oberfläche freigegeben wird.

Um private Daten für eine Oberfläche abzurufen, müssen Sie einen Puffer der richtigen Größe zuordnen und dann die GetPrivateData-Methode aufrufen und die GUID übergeben, die den Daten zugewiesen wurde. Sie sind dafür verantwortlich, jeglichen dynamischen Arbeitsspeicher freizugeben, den Sie für diesen Puffer verwenden. Wenn es sich bei den Daten um ein COM-Objekt handelt, ruft diese Methode den [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ab.

Wenn Sie nicht wissen, wie groß ein Puffer zugeordnet werden soll, rufen Sie zunächst GetPrivateData mit 0 (null) in pSizeOfData auf. Wenn die Methode mit D3DERR \_ MOREDATA fehlschlägt, wird die erforderliche Anzahl von Bytes für den Puffer zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
