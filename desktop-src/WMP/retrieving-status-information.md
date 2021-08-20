---
title: Abrufen von Statusinformationen
description: Abrufen von Statusinformationen
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player,Download-Manager
- Onlineshops,Download-Manager
- Typ 2 Onlineshops,Download-Manager
- Windows Media Player online stores,retrieving status
- Onlineshops,Abrufen des Status
- Typ 2 Onlineshops,Abrufen des Status
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Abrufen des Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa65627ce692e3287f777fc9c09fa797fcb25fe57c0e2b738ae3c066b62abeec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933710"
---
# <a name="retrieving-status-information"></a>Abrufen von Statusinformationen

Statusinformationen werden mit dem in der **Init-Funktion** erstellten Timer aktualisiert. Alle Status werden mit demselben Timer aktualisiert. Der Name der Funktion für das Timerereignis ist **OnTimer.**

**OnTimer bestimmt** die anzuzeigenden Informationen basierend auf der Benutzerauswahl, die in der globalen Variablen g \_ oCurrentDLItem gespeichert wird. Die Funktion testet zunächst, ob die Werte für Größe oder Status gültig sind, und erstellt eine Zeichenfolge für jeden Fall.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Wenn ein Wert gültig ist, stellt die Zeichenfolge die Byteanzahl dar. Wenn der Wert ungültig ist, z. B. -1, stellt die Zeichenfolge eine Meldung bereit, um den Benutzer darüber zu informieren, dass die Informationen noch nicht verfügbar sind.

Als Nächstes bestimmt **ein switch-Block,** ob der Download für das ausgewählte Element abgeschlossen oder abgebrochen wird. Wenn einer der Fälle true ist, wird der Wert der Variablen Größe oder Status entsprechend aktualisiert.


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



Schließlich werden die Statusinformationen im DIV-Element namens dlstate angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




