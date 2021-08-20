---
description: Gerätetransportstatus
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Gerätetransportstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ea7c3d6cba8363826c0fdab3cf411f0d68d6e284832a75c02cac3b1eefa770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952949"
---
# <a name="device-transport-state"></a>Gerätetransportstatus

Rufen Sie die [**IAMExtTransport::get \_ Mode-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) auf, um den aktuellen Zustand des Geräts abzurufen, z. B. Wiedergabe, Pause oder Beendigung. Die -Methode ruft eine Konstante ab, die den Gerätezustand angibt:



| Wert                    | Device State |
|--------------------------|--------------|
| WIEDERGABE \_ IM ED-MODUS \_           | Abspielen         |
| BEENDEN \_ DES ED-MODUS \_           | Beenden         |
| EINFRIEREN \_ DES ED-MODUS \_         | Anhalten        |
| \_ED-MODUS \_ FF             | Schnelle Weiterleitung |
| ED \_ MODE \_ REW            | Rewind       |
| DATENSATZ \_ IM ED-MODUS \_         | Datensatz       |
| EINFRIEREN \_ \_ DES DATENSATZES IM ED-MODUS \_ | Anhalten von Aufzeichnungen |



 

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

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



