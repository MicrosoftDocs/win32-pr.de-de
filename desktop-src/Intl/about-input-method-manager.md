---
description: Durch die Verwendung der imm-Funktionalität in ihrer IME-fähigen Anwendung können Benutzer alle möglichen Zeichen Werte merken.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Informationen über den Eingabemethoden-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353582"
---
# <a name="about-input-method-manager"></a>Informationen über den Eingabemethoden-Manager

Durch die Verwendung der imm-Funktionalität in ihrer IME-fähigen Anwendung können Benutzer alle möglichen Zeichen Werte merken. Stattdessen ermöglicht es dem IME, die Tastatureingaben eines Benutzers zu überwachen, die vom Benutzer gewünschten Zeichen zu erwarten und eine Liste von Kandidaten Zeichen zur Auswahl zu erhalten.

> [!Note]  
> Der imm führt ähnliche Vorgänge wie das [Text Services-Framework](../tsf/text-services-framework.md)aus, die von Anwendungen verwendet werden, die mit Text Diensten kommunizieren.

 

Standardmäßig stellt das IMM-Fenster ein IME-Fenster bereit, über das der Benutzer Tastatureingaben und Ansichten eingibt und Kandidaten auswählt. Anwendungen können die imm-Funktionen und-Nachrichten verwenden, um Ihre eigenen IME-Fenster zu erstellen und zu verwalten. dabei wird eine benutzerdefinierte Schnittstelle bereitgestellt, während die Konvertierungs Funktionen von

Der imm ist nur auf ostasiatischen, lokalisierten Windows-Betriebssystemen (Chinesisch, Japanisch, Koreanisch) aktiviert. Auf diesen Systemen Ruft die Anwendung [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ DbcsEnabled auf, um zu bestimmen, ob der imm aktiviert ist.

**Windows 2000:** In allen lokalisierten Sprachversionen ist eine Funktions Unterstützung mit vollem Funktionsumfang verfügbar. Der imm ist jedoch nur aktiviert, wenn ein asiatisches Sprachpaket installiert ist. Eine IME-fähige Anwendung kann [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit SM \_ immenabled aufrufen, um zu bestimmen, ob der imm aktiviert ist.

Dieses Thema enthält folgende Abschnitte:

-   [Kandidatenlisten](candidate-lists.md)
-   [Kompositions Zeichenfolge](composition-string.md)
-   [Hexin Unicode-IME](hextounicode-ime.md)
-   [Abkürzungstasten](hot-keys.md)
-   [IME-Nachrichten](ime-messages.md)
-   [IME-Fenster Klasse](ime-window-class.md)
-   [Eingabe Kontext](input-context.md)
-   [Fenster "Status", "Komposition" und "Kandidaten"](status--composition--and-candidates-windows.md)

 

 
