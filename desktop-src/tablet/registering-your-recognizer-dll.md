---
description: Ihre Erkennungs-DLL muss registriert sein, damit sie von der Tablet PC Platform verwendet werden kann. Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrieren der Erkennungs-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae80eb49f1795e315cf77bf5aede83cc1677e168f4aea4d6715a216e74434caf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350070"
---
# <a name="registering-your-recognizer-dll"></a>Registrieren der Erkennungs-DLL

Ihre Erkennungs-DLL muss registriert sein, damit sie von der Tablet PC Platform verwendet werden kann. Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.

Fügen Sie einen neuen Schlüssel für jede CLSIDs Ihrer Erkennung unter dem Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ hinzu. Fügen Sie eine CLSID pro Sprache hinzu. In der folgenden Tabelle werden die Werte beschrieben, die unter jedem der Schlüssel hinzugefügt werden sollen, die Ihre CLSIDs enthalten.

> [!Note]  
> Bei den Namen dieser Werte wird die Groß-/Kleinschreibung beachtet.

 



| Wertname                             | Werttyp             | Wertbeschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erkennungsfunktionsflags<br/> | REG \_ DWORD<br/>  | DWORD wird verwendet, um die Funktionen der Erkennung zu bestimmen.<br/>                                                                                                                                                                                                                                                                                                                             |
| Erkennungs-DLL<br/>              | REG \_ SZ<br/>     | Vollständiger Pfad zur installierten Erkennungs-DLL.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Erkannte Sprachen<br/>        | REG \_ BINARY<br/> | Binäres Array, das die Sprache oder Sprachen beschreibt, mit denen eine Erkennung verwendet werden kann.<br/> In rectypes.h gibt die MAX \_ LANGUAGES-Definition die maximale Anzahl von Sprachen an, die von einer Erkennung unterstützt werden, und jede Sprache verwendet ein WORD zum Speichern im Element "Erkannte Sprachen". Die Größe des \_ Registrierungseintrags REG BINARY sollte MAX LANGUAGES \_ \* sizeof(WORD) sein.<br/> |



 

 

 




