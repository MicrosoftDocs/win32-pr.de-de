---
title: Abrufen von Status Informationen
description: Abrufen von Status Informationen
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Abrufen des Status
- Online Stores, Abrufen des Status
- Typ 2 Online Stores, Status abrufen
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Abrufen des Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712720"
---
# <a name="retrieving-status-information"></a>Abrufen von Status Informationen

Status Informationen werden mithilfe des Zeit Gebers aktualisiert, der in der **Init** -Funktion erstellt wurde. Der gesamte Status wird mit demselben Zeitgeber aktualisiert. Der Name der Funktion für das Timer-Ereignis ist **OnTimer**.

**OnTimer** bestimmt die Informationen, die auf der Grundlage der Benutzer Auswahl angezeigt werden, die in der globalen Variablen "g \_ ocurrentdlitem" gespeichert ist. Die-Funktion testet zunächst, ob die Größe oder die Fortschritts Werte gültig sind, und erstellt für jeden Fall eine Zeichenfolge.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Wenn ein Wert gültig ist, stellt die Zeichenfolge die Byte Anzahl dar. Wenn der Wert nicht gültig ist, z. b.-1, stellt die Zeichenfolge eine Meldung bereit, um den Benutzer darüber zu informieren, dass die Informationen noch nicht verfügbar sind.

**Als Nächstes bestimmt ein** switchblock, ob der Download für das ausgewählte Element abgeschlossen oder abgebrochen wurde. Wenn einer der Fälle true ist, wird der Wert der Variablen Größe oder des Fortschritts entsprechend aktualisiert.


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



Schließlich werden die Statusinformationen im div-Element mit dem Namen "dlstate" angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




