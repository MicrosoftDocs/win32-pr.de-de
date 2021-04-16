---
description: Ihre Erkennungs-DLL muss für die Tablet PC-Plattform registriert sein, damit Sie verwendet werden kann. Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrieren der Erkennungs-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530275"
---
# <a name="registering-your-recognizer-dll"></a>Registrieren der Erkennungs-DLL

Ihre Erkennungs-DLL muss für die Tablet PC-Plattform registriert sein, damit Sie verwendet werden kann. Die Erkennung muss bei der Installation die folgenden Änderungen an der Registrierung vornehmen.

Fügen Sie unter dem HKEY \_ local \_ Machine/Software/Microsoft/TPG/erkenzers/Registry Key einen neuen Schlüssel für jede CLSIDs Ihres erkenners hinzu. Fügen Sie eine CLSID pro Sprache hinzu. In der folgenden Tabelle werden die Werte beschrieben, die unter allen Schlüsseln hinzugefügt werden sollen, die ihre CLSIDs enthalten.

> [!Note]  
> Bei den Namen dieser Werte wird die Groß-/Kleinschreibung beachtet.

 



| Wertname                             | Werttyp             | Wertbeschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funktionsflags für Erkennungsfunktionen<br/> | REG \_ DWORD<br/>  | DWORD, das verwendet wird, um die Funktionen der Erkennung zu bestimmen.<br/>                                                                                                                                                                                                                                                                                                                             |
| Erkennungs-DLL<br/>              | REG- \_ SZ<br/>     | Vollständiger Pfad zur installierten Erkennungs Modul-dll.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Erkannte Sprachen<br/>        | REG- \_ Binärdatei<br/> | Binäres Array, das die Sprache oder die Sprachen beschreibt, mit denen eine Erkennung arbeiten soll.<br/> In "rectypes. h \_ " gibt die maximale Anzahl von Sprachen an, die maximale Anzahl von Sprachen, die von einer Erkennung unterstützt werden, und jede Sprache nimmt ein Wort an, das im Element "erkannte Sprachen" gespeichert wird. Die Größe des \_ Registrierungs Eintrags "reg Binary" sollte "Max \_ Languages \* sizeof (Word)" lauten.<br/> |



 

 

 




