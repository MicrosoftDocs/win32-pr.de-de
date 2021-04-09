---
description: Anwendungs Kontexte können zum Erstellen paralleler Windows-Klassen verwendet werden.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Erstellen paralleler Windows-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866023"
---
# <a name="creating-side-by-side-windows-classes"></a>Erstellen paralleler Windows-Klassen

Anwendungs Kontexte können zum Erstellen paralleler Windows-Klassen verwendet werden. Wenn Sie parallele Windows-Klassen verwenden, kann die Anwendung unterschiedliche Versionen einer Klasse gleichzeitig in einem übergeordneten Fenster verwenden. Um eine Seite-an-Seite-Windows-Klasse zu erstellen, muss Ihre Anwendung vor dem Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) einen Aktivierungs Kontext aktivieren, um ein Handle für das neue Fenster zu erhalten.

Beispielsweise hatten die allgemeinen Windows-Steuerelemente Version 5,82 und Version 6,0 ein Bearbeitungs Steuerelement. Standardmäßig verwendet Windows das Bearbeitungs Steuerelement der Version 5,82. Um ein paralleles Fenster zu erhalten, das über das Bearbeitungs Steuerelement der Version 6,0 verfügt, kann die Anwendung vor dem Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) wie gewohnt auf eine Assembly verweisen, die benannte Fenster Klassen verfügbar macht, und dann den Aktivierungs Kontext aktivieren, der auf die Steuerelemente der Version 6,0 verweist.

 

 
