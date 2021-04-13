---
title: Input-Active-Client
description: Input-Active-Client
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310667"
---
# <a name="input-active-client"></a>Input-Active-Client

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Da mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden können und mehrere Clients gleichzeitig verschiedene Zeichen verwenden können, legt der Server einen Client als *Eingabe aktiven* Client fest und sendet Maus-und Spracheingaben nur an diese Client Anwendung. Dadurch wird die ordnungsgemäße Verwaltung von Benutzereingaben aufrechterhalten, sodass ein entsprechender Client auf die Eingabe antwortet.

In der Regel bestimmt die Benutzerinteraktion, welche Client Anwendung als Eingabe aktiv wird. Wenn der Benutzer z. b. auf ein Zeichen klickt, wird die Client Anwendung dieses Zeichens als Eingabe aktiv. Ebenso gilt: Wenn ein Benutzer den Namen eines Zeichens spricht, wird er als Eingabe aktiv. Wenn der Server außerdem die [**Show**](show-method.md) -Methode eines Zeichens verarbeitet, wird der Client dieses Zeichens als Eingabe aktiv.

Wenn ein Zeichen ausgeblendet wird, ist der Client dieses Zeichens für dieses Zeichen nicht mehr als Eingabe aktiv. Der Server stellt den aktiven Client automatisch für alle verbleibenden Zeichen (s) ein. Wenn alle Zeichen ausgeblendet sind, ist kein Client Eingabe aktiv. Wenn der Benutzer jedoch in dieser Situation den abzurufenden Hotkey drückt, lauscht der-Agent weiterhin auf seine Befehle (mithilfe der sprach Erkennungs-Engine, die mit dem obersten Zeichen des letzten Eingabe aktiven Clients übereinstimmt).

Wenn mehrere Clients dasselbe Zeichen gemeinsam nutzen, wird der *aktive Client* vom Server als aktiver Eingabe Client bezeichnet. Das aktive Zeichen ist die oberste Position in der Client Reihenfolge. Mithilfe der Methode [**aktivieren**](activate-method.md) können Sie den Client als aktiven oder nicht aktiven Client festlegen. Sie können auch die Methode **aktivieren** verwenden, um die Client Eingabe-aktiv zu machen. um die Unterbrechung anderer Clients des Zeichens zu vermeiden, sollten Sie dies jedoch nur dann tun, wenn die Client Anwendung aktiv ist. Wenn der Benutzer z. b. auf das Fenster der Anwendung klickt und die Anwendung aktiviert, können Sie die **Aktivierungs** Methode aufrufen, um die Maus-und Spracheingaben zu empfangen und zu verarbeiten, die an das Zeichen weitergeleitet werden.

 

 




