---
description: Die Smartcard-Benutzeroberfläche (Ui) ist ein einzelnes allgemeines Dialogfeld, in dem der Benutzer angeben oder nach einer Smartcard suchen kann, die geöffnet werden soll (d. b. eine Verbindung mit einer Anwendung herstellen und sie in einer Anwendung verwenden).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Smartcard-Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b94a82889d196b01f8a1d1ca6af7b4788398d9508accc2d5ca245f7929d9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917330"
---
# <a name="smart-card-user-interface"></a>Smartcard-Benutzeroberfläche

Die [*Smartcard-Benutzeroberfläche*](../secgloss/u-gly.md) (Ui) ist ein einzelnes [*allgemeines Dialogfeld,*](../secgloss/s-gly.md) in dem der Benutzer angeben oder nach einer Smartcard suchen kann, die geöffnet werden soll (d. b. eine Verbindung mit einer Anwendung herstellen und sie in einer Anwendung verwenden).

Im Folgenden finden Sie zwei Möglichkeiten, wie Sie das allgemeine Dialogfeld verwenden können. Beide gehen davon aus, dass die Benutzeroberfläche des Dialogfelds angezeigt wird. Weitere Informationen finden Sie unter [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**So wählen Sie eine zu öffnende Smartcard aus**

1.  Deklarieren Sie eine Variable vom Typ **OPENCARDNAME**.
2.  Stellen Sie genügend Informationen im allgemeinen Dialogfeld bereit, um die Suche nach einer Smartcard einzugrenzen, nach der die aufrufende Anwendung sucht. Dies schließt die Angabe von **lpstrGroupNames,** **lpstrCardNames** und **rgguidInterfaces ein.** Dies umfasst auch die Angabe eines bevorzugten Freigabemodus und Protokolls, der verwendet werden soll, wenn das allgemeine Dialogfeld mithilfe der **Member dwShareMode** und **dwPreferredProtocols** der [**OPENCARDNAME-Struktur**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) eine Verbindung mit der Karte herstellt.
3.  Rufen Sie die [**GetOpenCardName-Funktion**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) auf, um dem Benutzer das allgemeine Dialogfeld anzuzeigen. Eine einfache Hilfeinformationszeile wird angezeigt, und wenn eine der angeforderten Karten gefunden wird, wird die Karte in der Anzeige hervorgehoben. Bei Suchvorgängen mit mehreren Kartennamen wird der erste Leser, der eine der bevorzugten Karten enthält, hervorgehoben.
4.  Der Benutzer wählt dann eine Karte aus, klickt auf **OK** und stellt eine Verbindung mit der Smartcard her.

**So suchen Sie nach einer bestimmten Karte**

1.  Deklarieren Sie eine Variable vom Typ **OPENCARDNAME**.
2.  Stellen Sie genügend Informationen im allgemeinen Dialogfeld bereit, um die Suche nach einer Smartcard einzugrenzen, nach der die aufrufende Anwendung sucht. Dies schließt die Angabe von **lpstrGroupNames,** **lpstrCardNames** und **rgguidInterfaces ein.**
3.  Erstellen Sie die **Rückruffunktionen Verbinden**, **Check** und **Disconnect,** und legen Sie die Datenmember **lpfnConnect,** **lpfnCheck** und **lpfnDisconnect** entsprechend fest.
    > [!Note]  
    > Alle drei Funktionen und Member müssen verfügbar sein, wenn das allgemeine Dialogfeld auf diese Weise verwendet wird.

     

4.  Rufen Sie die allgemeine Dialogfeldfunktion [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) auf.
5.  Das allgemeine Dialogfeld sucht dann nach den angeforderten Karten. Wenn ein übereinstimmender Kartenname oder eine [*entsprechende ATR-Zeichenfolge*](../secgloss/a-gly.md) gefunden wird, werden die Rückruffunktionen **Verbinden**, **Check** und **Disconnect** nacheinander aufgerufen. Wenn eine Karte die **Check-Routine** übergibt (d. h. der **Check-Rückruf** gibt **TRUE** zurück), wird diese Karte für den Benutzer in der Anzeige hervorgehoben.
    > [!Note]  
    > Wenn mehrere Kartennamen angegeben werden, ist der erste Leser, der eine der angeforderten Karten enthält und die **Check-Routine** übergibt, die ausgewählte Karte.

     

6.  Wenn keine Übereinstimmungen gefunden werden, wird ein allgemeines Dialogfeld angezeigt.

 

 
