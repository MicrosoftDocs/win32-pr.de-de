---
description: Jeder Thread kann ein Fenster erstellen.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Erstellen von Windows in Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2084536ff43ea4c52efb179177fe6f6c803c49b9f580b2d298b73e9b528f1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143093"
---
# <a name="creating-windows-in-threads"></a>Erstellen von Windows in Threads

Jeder Thread kann ein Fenster erstellen. Der Thread, der das Fenster erstellt, besitzt das Fenster und die zugehörige Nachrichtenwarteschlange. Daher muss der Thread eine Nachrichtenschleife bereitstellen, um die Nachrichten in seiner Nachrichtenwarteschlange zu verarbeiten. Darüber hinaus müssen Sie [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) oder [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in diesem Thread anstelle der anderen [Wartefunktionen](/windows/desktop/Sync/wait-functions)verwenden, damit Nachrichten verarbeitet werden können. Andernfalls kann ein Deadlock des Systems auftreten, wenn dem Thread während des Wartens eine Nachricht gesendet wird.

Die [**AttachThreadInput-Funktion**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) kann verwendet werden, um einer Gruppe von Threads zu ermöglichen, denselben Eingabezustand zu verwenden. Durch die Freigabe des Eingabezustands teilen sich die Threads ihr Konzept des aktiven Fensters. Dadurch kann ein Thread immer das Fenster eines anderen Threads aktivieren. Diese Funktion ist auch nützlich, um den Fokuszustand, den Mauserfassungszustand, den Tastaturzustand und den Z-Reihenfolgenzustand des Fensters für Fenster freizugeben, die von verschiedenen Threads erstellt wurden, deren Eingabezustand gemeinsam genutzt wird.

Informationen zum Erstellen von Fenstern finden Sie unter [Windows Klassen](../winmsg/window-classes.md).

 

 
