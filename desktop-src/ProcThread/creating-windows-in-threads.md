---
description: Jeder Thread kann ein Fenster erstellen.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Erstellen von Fenstern in Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367936"
---
# <a name="creating-windows-in-threads"></a>Erstellen von Fenstern in Threads

Jeder Thread kann ein Fenster erstellen. Der Thread, der das Fenster erstellt, besitzt das Fenster und die zugehörige Meldungs Warteschlange. Daher muss der Thread eine Nachrichten Schleife bereitstellen, um die Nachrichten in der Nachrichten Warteschlange zu verarbeiten. Außerdem müssen Sie in diesem Thread [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) oder [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) verwenden, damit Nachrichten [verarbeitet werden können](/windows/desktop/Sync/wait-functions). Andernfalls kann das System blockiert werden, wenn dem Thread beim warten eine Nachricht gesendet wird.

Die [**attachthreadinput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) -Funktion kann verwendet werden, um zuzulassen, dass eine Gruppe von Threads denselben Eingabe Zustand verwendet. Durch die Freigabe des Eingabe Zustands teilen die Threads ihr Konzept des aktiven Fensters. Auf diese Weise kann ein Thread immer das Fenster eines anderen Threads aktivieren. Diese Funktion eignet sich auch zum Freigeben des Fokus Zustands, des Maus Erfassungs Zustands, des Tastatur Zustands und des Fenster-Z-Reihen folgen Zustands zwischen Fenstern, die von verschiedenen Threads erstellt wurden, deren Eingabe Zustand freigegeben ist.

Weitere Informationen zum Erstellen von Windows finden Sie unter [Windows-Klassen](../winmsg/window-classes.md).

 

 
