---
title: Abrufen der System Zeit
description: Abrufen der System Zeit
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Multimedia-Timer, Systemzeit
- Timer, Systemzeit
- Systemuhrzeit
- timeGetTime-Funktion
- timegetsystemtime-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472820"
---
# <a name="obtaining-the-system-time"></a>Abrufen der System Zeit

Bevor eine Anwendung mit der Verwendung der Multimediatimer-Dienste beginnt, wird in der Regel die aktuelle *Systemzeit* abgerufen. Die Systemzeit ist die Zeit (in Millisekunden), seit der das Microsoft Windows-Betriebssystem gestartet wurde. Sie können die [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) -Funktion oder die [**timegetsystemtime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) -Funktion verwenden, um die Systemzeit abzurufen. Diese beiden Funktionen sind sehr ähnlich: **timeGetTime** gibt die Systemzeit zurück, und **timegetsystemtime** füllt eine [**mmtime**](/previous-versions//dd757347(v=vs.85)) -Struktur mit der Systemzeit.

 

 