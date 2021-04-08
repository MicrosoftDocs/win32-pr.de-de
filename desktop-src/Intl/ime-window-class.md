---
description: Die IME-Fenster Klasse ist eine vordefinierte globale System Klasse, die die Darstellung und das Verhalten der standardmäßigen IME-Fenster definiert.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: IME-Fenster Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865500"
---
# <a name="ime-window-class"></a>IME-Fenster Klasse

Die IME-Fenster Klasse ist eine vordefinierte globale System Klasse, die die Darstellung und das Verhalten der standardmäßigen IME-Fenster definiert. Die-Klasse ähnelt allgemeinen Steuerelement Klassen darin, dass die Anwendung ein Fenster dieser Klasse mithilfe [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion" erstellt. Ebenso wie statische Steuerelemente antwortet ein IME-Fenster nicht auf Benutzereingaben. Stattdessen benachrichtigt Sie den IME über Benutzereingabe Aktionen und verarbeitet die von der IME-oder-Anwendungen an ihn gesendeten Nachrichten, um eine Antwort auf die Benutzeraktion auszuführen.

IME-fähige Anwendungen erstellen manchmal angepasste IME-Fenster mithilfe der IME-Fenster Klasse. Durch die Verwendung der Fenster Anpassung kann die Anwendung die Standard Verarbeitung des IME-Fensters nutzen, während Sie die Kontrolle über die Fenster Positionierung hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 
