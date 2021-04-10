---
description: Eine Liste mit einigen der möglichen Rückgabecodes für Methoden und Funktionen.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4146a65e9092dcd3fed261c127e84fe8552128a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213882"
---
# <a name="s_present"></a>S \_ vorhanden

Eine Liste mit einigen der möglichen Rückgabecodes für Methoden und Funktionen.



|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| S \_ OK                     | Das Gerät wird normal ausgeführt und kann zum Rendern verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| S \_ sind \_ okkludiert.      | Der Präsentationsbereich ist okkludiert. "Oksion" bedeutet, dass das Präsentations Fenster minimiert ist oder ein anderes Gerät in den Vollbildmodus auf demselben Monitor wie das Präsentations Fenster und das Präsentations Fenster vollständig auf diesem Monitor angezeigt wird. Die Okklusion tritt nicht auf, wenn der Client Bereich von einem anderen Fenster abgedeckt wird.<br/> Okdierte Anwendungen können das Rendering fortsetzen, und alle Aufrufe werden erfolgreich ausgeführt, aber das Fenster für die okkludierte Darstellung wird nicht aktualisiert. Vorzugsweise sollte die Anwendung das Rendern im Präsentations Fenster mithilfe des Geräts übernehmen und den Aufruf von [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) fortsetzen, bis s OK ist, oder wenn der \_ \_ \_ Modus \_ geändert wird.<br/> |
| S der \_ aktuelle \_ Modus \_ geändert | Der Desktop Anzeigemodus wurde geändert. Die Anwendung kann das Rendering fortsetzen, aber es kann eine Farbkonvertierung/-Streckung vorhanden sein. Wählen Sie ein backpufferformat aus, das dem aktuellen Anzeigemodus ähnelt, und kehren Sie zum erneuten Erstellen der Austausch Ketten zurück. Das Gerät verlässt diesen Zustand, nachdem eine zurück Setzung aufgerufen wurde.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Andere Fehlercodes sind in [D3DERR](d3derr.md)enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




