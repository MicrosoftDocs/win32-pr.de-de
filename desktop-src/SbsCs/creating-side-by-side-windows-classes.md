---
description: Anwendungskontexte können verwendet werden, um Windows Klassen nebeneinander zu erstellen.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Erstellen von klassenseitigen Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8317712b333963f9864e195bb1c5f18896dcd73eec059c9c4ae670ff2fb6a4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142343"
---
# <a name="creating-side-by-side-windows-classes"></a>Erstellen von klassenseitigen Windows

Anwendungskontexte können verwendet werden, um Windows Klassen nebeneinander zu erstellen. Wenn Sie parallele Windows Klassen verwenden, kann Ihre Anwendung unterschiedliche Versionen einer Klasse gleichzeitig in einem einzigen übergeordneten Fenster aktiv haben. Um eine Windows Klasse zu erstellen, muss Ihre Anwendung vor dem Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) einen Aktivierungskontext aktivieren, um ein Handle für das neue Fenster abzurufen.

Beispielsweise verfügten Windows Common Controls Version 5.82 und Version 6.0 über ein Edit-Steuerelement. Windows verwendet standardmäßig das Bearbeitungssteuerelement der Version 5.82. Um ein nebeneinanderliegendes Fenster mit dem Edit-Steuerelement der Version 6.0 abzurufen, kann Ihre Anwendung vor dem üblichen Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) auf eine Assembly verweisen, die benannte Fensterklassen verfügbar macht, und dann den Aktivierungskontext aktivieren, der auf die Steuerelemente der Version 6.0 verweist.

 

 
