---
description: Der Fehler Modus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren wird.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Fehler Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125714"
---
# <a name="error-mode"></a>Fehler Modus

Der Fehler Modus gibt dem System an, wie die Anwendung auf schwerwiegende Fehler reagieren wird. Schwerwiegende Fehler sind u. a. Datenträger Fehler, nicht fertige Laufwerke, falsche Daten Ausrichtung und nicht behandelte Ausnahmen. Dieser Fehler Modus kann entweder pro Thread oder pro Prozess verwaltet werden. Eine Anwendung kann es dem System ermöglichen, ein Meldungs Feld anzuzeigen, in dem der Benutzer informiert wird, dass ein Fehler aufgetreten ist, oder er kann die Fehler behandeln.

Verwenden Sie [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) oder den Thread spezifischen [**setthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode), um diese Fehler ohne Benutzereingriff zu behandeln. Nachdem eine dieser Funktionen aufgerufen und entsprechende Flags angegeben wurden, werden die entsprechenden Fehlermeldungs Felder vom System nicht angezeigt.

Ein Prozess kann seinen Fehler Modus mithilfe von [**geterrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) oder [**getthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)abrufen.

Die bewährte Vorgehensweise besteht darin, dass alle Anwendungen beim Start die Prozess weite Funktion " [**setterrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) " mit dem Parameter " **SEM \_ failcriticalerrors** " aufrufen. Dadurch wird verhindert, dass die Anwendung im fehlermodusdialogfelder angezeigt wird.

Abgesehen davon sollten Aufrufer die Thread spezifischen Versionen dieser Funktionen bevorzugen, da Sie das normale Systemverhalten weniger stören.

 

 
