---
description: Die Smartcard-Benutzeroberfläche (User Interface, UI) ist ein einzelnes, gängiges Dialogfeld, mit dem der Benutzer eine Smartcard angeben oder suchen kann, die geöffnet werden soll (d. h. eine Verbindung mit einer Anwendung herstellen und diese verwenden)
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Smartcard-Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350024"
---
# <a name="smart-card-user-interface"></a>Smartcard-Benutzeroberfläche

Die Smartcard- [*Benutzeroberfläche (User Interface*](../secgloss/u-gly.md) , UI) ist ein einzelnes, [*gängiges Dialogfeld*](../secgloss/s-gly.md) , mit dem der Benutzer eine Smartcard angeben oder suchen kann, die geöffnet werden soll (d. h. eine Verbindung mit einer Anwendung herstellen und diese verwenden)

Im folgenden finden Sie zwei Möglichkeiten, wie Sie das Dialogfeld "Allgemein" verwenden können. Beide gehen davon aus, dass die Benutzeroberfläche des Dialog Felds angezeigt wird. Weitere Informationen finden Sie unter [**opencardname**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**So wählen Sie eine Smartcard aus, die geöffnet werden soll**

1.  Deklarieren Sie eine Variable vom Typ **opencardname**.
2.  Geben Sie im Dialogfeld "Allgemein" genügend Informationen an, um die Suche nach einer Smartcard einzuschränken, nach der die aufrufende Anwendung sucht. Dies umfasst das Angeben von **lpstringroupnames**, **lpstrancardnames** und **rgguidinterfaces**. Dies umfasst auch die Angabe eines bevorzugten Freigabe Modus und Protokolls, die verwendet werden sollen, wenn das allgemeine Dialogfeld mithilfe der **dwsharemode** -und **dwpreferredprotokolls** -Member der Struktur von [**opencardname**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) eine Verbindung mit der Karte herstellt.
3.  Aufrufen der [**getopencardname**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) -Funktion, um dem Benutzer das allgemeine Dialogfeld anzuzeigen. Eine einfache Hilfe Informations Zeile wird angezeigt, und wenn eine der angeforderten Karten gefunden wird, wird die Karte in der Anzeige hervorgehoben. Bei mehreren Kartennamen suchen wird der erste Reader, der eine der bevorzugten Karten enthält, hervorgehoben.
4.  Der Benutzer wählt dann eine Karte aus, klickt auf **OK** und stellt eine Verbindung mit der Smartcard her.

**So suchen Sie nach einer bestimmten Karte**

1.  Deklarieren Sie eine Variable vom Typ **opencardname**.
2.  Geben Sie im Dialogfeld "Allgemein" genügend Informationen an, um die Suche nach einer Smartcard einzuschränken, nach der die aufrufende Anwendung sucht. Dies umfasst das Angeben von **lpstringroupnames**, **lpstrancardnames** und **rgguidinterfaces**.
3.  Erstellen Sie die Rückruf Funktionen **Connect**, **Check** und **Disconnect** , und legen Sie die Datenmember **lpfnconnect**, **lpfncheck** und **lpfndisconnect** entsprechend fest.
    > [!Note]  
    > Alle drei Funktionen und Member müssen verfügbar sein, wenn Sie das allgemeine Dialogfeld auf diese Weise verwenden.

     

4.  Aufrufen der Funktion " [**getopencardname**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) " (allgemeine Dialogfeld).
5.  Im Dialogfeld Allgemein wird dann nach den angeforderten Karten gesucht. Wenn ein passender Kartenname oder eine [*ATR-Zeichenfolge*](../secgloss/a-gly.md) gefunden wird, werden die Rückruf Funktionen **Connect**, **Check** und **Disconnect** nacheinander aufgerufen. Wenn eine Karte die **Check** -Routine übergibt (d. h., der **Check** -Rückruf gibt **true** zurück), wird diese Karte in der Anzeige für den Benutzer hervorgehoben.
    > [!Note]  
    > Wenn mehrere Kartennamen angegeben werden, wird der erste Reader, der eine der angeforderten Karten enthält und die **Check** -Routine übergibt, die ausgewählte Karte.

     

6.  Wenn keine Übereinstimmungen gefunden werden, wird ein gemeinsames Dialogfeld angezeigt.

 

 
