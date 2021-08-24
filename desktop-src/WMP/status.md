---
title: Status (Windows Media Player SDK)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Windows Media Player Mobile Skins, Statusanzeige
- Skins, Statusanzeige
- Referenz für Skins, Statusanzeige
- Statusanzeige in Skins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc4ca5db8da51cc00b99c91b8bdf77728089e82583f39828f869f24dab8c6c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832437"
---
# <a name="status-windows-media-player-sdk"></a>Status (Windows Media Player SDK)

Möglicherweise möchten Sie eine Statusanzeige in Ihrer Skin verwenden. In diesem Zustand muss das Statuselement in der Skindefinitionsdatei definiert werden. Alternativ können Sie diese Informationen auch mithilfe des Status-Attributs im Text -Element anzeigen.

Der Abschnitt Status der Skindefinitionsdatei beginnt mit dieser Zeile:


```C++
[ Status ]

```



Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zur Statusanzeige in Ihrer Skin enthalten.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Sie können die folgende Vorlage für den Abschnitt Status Ihrer Skindefinitionsdatei verwenden:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Sie müssen die in der vorherigen Vorlage gezeigte Reihenfolge für Statusanzeigeinformationen für jede Zeile im Abschnitt Status verwenden. Jeder Teil der Zeile ist erforderlich. In den folgenden Abschnitten wird jedes Element beschrieben:

-   [Angezeigter Status](status-item.md)
-   [Statusspeicherort](status-location.md)
-   [Statusausrichtung](status-alignment.md)
-   [Statusschriftart](status-font.md)
-   [Statusfarbe](status-color.md)

Ein Beispiel für den Statuscode finden Sie im [Abschnitt "Beispielstatus".](sample-status-section.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




