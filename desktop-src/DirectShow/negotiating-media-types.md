---
description: Aushandeln von Medientypen
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Aushandeln von Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361771"
---
# <a name="negotiating-media-types"></a>Aushandeln von Medientypen

Wenn der Filter Graph-Manager die [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) -Methode aufruft, verfügt er über mehrere Optionen zum Angeben eines Medientyps:

-   **Complete Type:** Wenn der Medientyp vollständig angegeben ist, versuchen die Pins, eine Verbindung mit diesem Typ herzustellen. Wenn dies nicht möglich ist, schlägt der Verbindungsversuch fehl.
-   **Partieller Medientyp:** Ein Medientyp ist *partiell* , wenn der Haupttyp, der Untertyp oder der Formattyp GUID \_ NULL ist. Der Wert GUID \_ Null fungiert als "Platzhalter", der angibt, dass ein beliebiger Wert zulässig ist. Die Pins verhandeln einen Typ, der mit dem partiellen Typ konsistent ist.
-   **Kein Medientyp:** Wenn der Filter Diagramm-Manager einen **null** -Zeiger übergibt, können die Pins allen Medientypen zustimmen, die für beide Pins zulässig sind.

Wenn die Pins eine Verbindung herstellen, verfügt die Verbindung immer über einen kompletten Medientyp. Der Medientyp, der vom Filter Graph-Manager angegeben wird, besteht darin, die möglichen Verbindungstypen einzuschränken.

Während des Aushandlungs Prozesses schlägt die Ausgabe-PIN einen Medientyp vor, indem die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) -Methode der Eingabe-PIN aufgerufen wird. Die Eingabe-PIN kann den vorgeschlagenen Typ akzeptieren oder ablehnen. Dieser Prozess wird wiederholt, bis entweder die Eingabe-PIN einen Typ annimmt, oder wenn die Ausgabe-PIN nicht mehr von den Typen ausgeht und die Verbindung fehlschlägt.

Gibt an, wie eine Ausgabe-PIN die anzuzeigende Medientypen auswählt. In den DirectShow-Basisklassen Ruft die Ausgabepin [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) auf der Eingabe-PIN auf. Diese Methode gibt einen Enumerator zurück, der die bevorzugten Medientypen der Eingabe-PIN auflistet. Wenn ein Fehler auftritt, listet die Ausgabe-PIN die eigenen bevorzugten Typen auf.

**Arbeiten mit Medientypen**

Überprüfen Sie in jeder Funktion, die einen **am- \_ \_ Medientyp** -Parameter empfängt, immer die Werte von **cbformat** und **Format Type** , bevor Sie den **pbformat** -Member dereferenzieren. Der folgende Code ist falsch:


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



Der folgende Code ist korrekt:


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



