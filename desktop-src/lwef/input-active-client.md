---
title: Input-Active Client
description: Input-Active Client
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9555b614a30e73df0cc7d1d81cd8192480d49261a32e8be8d164bdb277e4c0f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943960"
---
# <a name="input-active-client"></a>Input-Active Client

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Da mehrere Clientanwendungen das gleiche Zeichen verwenden können und mehrere Clients unterschiedliche Zeichen gleichzeitig verwenden können, legt der Server einen Client als *eingabeaktiven* Client fest und sendet Maus- und Spracheingaben nur an diese Clientanwendung. Dadurch wird die geordnete Verwaltung von Benutzereingaben verwaltet, sodass ein entsprechender Client auf die Eingabe reagiert.

In der Regel bestimmt die Benutzerinteraktion, welche Clientanwendung eingabeaktiv wird. Wenn der Benutzer beispielsweise auf ein Zeichen klickt, wird die Clientanwendung dieses Zeichens eingabeaktiv. Wenn ein Benutzer den Namen eines Zeichens spricht, wird er entsprechend eingabeaktiv. Wenn der Server außerdem die [**Show-Methode**](show-method.md) eines Zeichens verarbeitet, wird der Client dieses Zeichens eingabeaktiv.

Wenn ein Zeichen ausgeblendet ist, ist der Client dieses Zeichens für dieses Zeichen nicht mehr eingabeaktiv. Der Server macht den aktiven Client aller verbleibenden Zeichen automatisch als eingabeaktiv. Wenn alle Zeichen ausgeblendet sind, ist kein Client eingabeaktiv. Wenn der Benutzer in dieser Situation jedoch den Hotkey Lauschend drückt, lauscht der -Agent weiterhin auf seine Befehle (mithilfe der Spracherkennungs-Engine, die dem obersten Zeichen des letzten eingabeaktiven Clients entspricht).

Wenn mehrere Clients das gleiche Zeichen gemeinsam verwenden, legt der Server seinen *aktiven Client* als eingabeaktiven Client bereit. Das aktive Zeichen ist das oberste Zeichen in der Clientreihenfolge. Sie können ihren Client mithilfe der [**Activate-Methode**](activate-method.md) auf den aktiven oder nicht aktiven Client festlegen. Sie können auch die **Activate-Methode** verwenden, um den Client explizit als eingabeaktiv zu definieren. Um jedoch zu vermeiden, dass andere Clients des Zeichens unterbrochen werden, sollten Sie dies nur tun, wenn Ihre Clientanwendung aktiv ist. Wenn der Benutzer beispielsweise auf das Fenster Ihrer Anwendung klickt und Ihre Anwendung aktiviert, können Sie die **Activate-Methode** aufrufen, um Maus- und Spracheingaben zu empfangen und zu verarbeiten, die an das Zeichen weitergeleitet werden.

 

 




