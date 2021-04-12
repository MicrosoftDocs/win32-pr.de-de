---
description: Geräte Transport Status
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Geräte Transport Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392894"
---
# <a name="device-transport-state"></a>Geräte Transport Status

Um den aktuellen Zustand des Geräts abzurufen, z. b. wiedergeben, anhalten oder anhalten, rufen Sie die Methode [**IAMExtTransport:: get \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) auf. Die-Methode ruft eine Konstante ab, die den Gerätezustand angibt:



| Wert                    | Device State |
|--------------------------|--------------|
| \_Play-Modus wiedergeben \_           | Abspielen         |
| Ed- \_ Modus wird \_ beendet           | Stop         |
| Einfrieren des ED- \_ Modus \_         | Anhalten        |
| Ed- \_ Modus- \_ FF             | Schnell vorwärts |
| REW im ED- \_ Modus \_            | Rewind       |
| Datensatz im ED- \_ Modus \_         | Datensatz       |
| \_ \_ Daten Satz \_ Sperrung im ED-Modus | Datensatz-Pause |



 

Der folgende Code überprüft den Gerätestatus:


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



