---
description: Der Fehlermodus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren soll.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Fehlermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1baa4c0bc4e1209586b630f2a58bfb06572131de8e7d2706614c78646d7e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260930"
---
# <a name="error-mode"></a>Fehlermodus

Der Fehlermodus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren soll. Zu den schwerwiegenden Fehlern zählen Datenträgerfehler, Fehler ohne Laufwerksgröße, falsche Datenausstellung und nicht behandelte Ausnahmen. Dieser Fehlermodus kann entweder pro Thread oder pro Prozess verwaltet werden. Eine Anwendung kann es dem System gestatten, ein Meldungsfeld anzuzeigen, das den Benutzer darüber informiert, dass ein Fehler aufgetreten ist, oder die Fehler behandeln.

Verwenden Sie [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) oder den threadspezifischen [**SetThreadErrorMode,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)um diese Fehler ohne Benutzereingriff zu behandeln. Nachdem eine dieser Funktionen und die entsprechenden Flags angegeben wurden, zeigt das System die entsprechenden Fehlermeldungsfelder nicht an.

Ein Prozess kann seinen Fehlermodus mit [**GetErrorMode oder**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) [**GetThreadErrorMode abrufen.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)

Die bewährte Methode ist, dass alle Anwendungen die prozessweite [**SetErrorMode-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) mit dem Parameter **SEM \_ FAILCRITICALERRORS beim** Start aufrufen. Dadurch soll verhindert werden, dass Dialoge im Fehlermodus die Anwendung hängen.

Im Gegensatz dazu sollten Aufrufer die threadspezifischen Versionen dieser Funktionen bevorzugen, da sie weniger störend für das normale Verhalten des Systems sind.

 

 
