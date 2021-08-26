---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdae2465ccc9e7153a0e9cc8202027137e2a7c0f07fdfb5da2a83a7c0d1ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962240"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Ruft die Ursache des sichtbaren Zustands des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Die Adresse einer Variablen, die die Ursache für die letzte Änderung des Sichtbarkeitszustands des Zeichens empfängt und eine der folgenden Variablen ist:



| Wert                                                                   | BESCHREIBUNG                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0;**<br/>                 | Das Zeichen wurde nicht angezeigt.                                                               |
| **const unsigned short** **UserHid = 1;**<br/>                    | Der Benutzer hat das Zeichen mit dem Popupmenü des Taskleistensymbols des Zeichens oder mithilfe der Spracheingabe verborgen. |
| **const unsigned short** **UserShowed = 2;**<br/>                 | Der Benutzer hat das Zeichen angezeigt.                                                                  |
| **const unsigned short** **ProgramHid = 3;**<br/>                 | Die Anwendung hat das Zeichen verborgen.                                                         |
| **const unsigned short** **ProgramShowed = 4;**<br/>              | Die Anwendung hat das Zeichen gezeigt.                                                      |
| **const unsigned short** **OtherProgramHid = 5;**<br/>            | Eine andere Anwendung hat das Zeichen verborgen.                                                      |
| **const unsigned short** **OtherProgramShowed = 6;**<br/>         | Das Zeichen wurde in einer anderen Anwendung gezeigt.                                                   |
| **const unsigned short** **UserHidViaCharacterMenu = 7**<br/>     | Der Benutzer hat das Zeichen im Popupmenü des Zeichens verborgen.                                    |
| **const unsigned short** **UserHidViaTaskbarIcon = UserHid**<br/> | Der Benutzer hat das Zeichen mit dem Popupmenü des Taskleistensymbols des Zeichens oder mithilfe der Spracheingabe verborgen. |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





