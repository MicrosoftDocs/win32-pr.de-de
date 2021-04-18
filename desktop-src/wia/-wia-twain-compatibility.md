---
description: WIA stellt eine TWAIN-Kompatibilitäts Ebene bereit, die es TWAIN-fähigen Anwendungen ermöglicht, mit Windows-Abbild Erfassungs Geräten (WIA) zu kommunizieren.
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: TWAIN-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347192"
---
# <a name="twain-compatibility"></a>TWAIN-Kompatibilität

WIA stellt eine TWAIN-Kompatibilitäts Ebene bereit, die es TWAIN-fähigen Anwendungen ermöglicht, mit Windows-Abbild Erfassungs Geräten (WIA) zu kommunizieren. TWAIN-kompatible Anwendungen haben keinen vollständigen Zugriff auf die WIA-Funktionalität. Beispielsweise kann eine Anwendung die Benutzeroberfläche nicht mithilfe der TWAIN-Kompatibilitätsschicht unterdrücken.

WIA-Geräte werden zweimal für eine Anwendung angezeigt, die sowohl WIA als auch TWAIN kennt: einmal durch normale WIA-Kommunikation und einmal über die TWAIN-Kompatibilitätsschicht. Um das doppelte Auflisten eines WIA-Geräts zu vermeiden, muss eine Anwendung, die sowohl WIA als auch TWAIN kennt, die WIA-Geräte herausfiltern, die über die TWAIN-Kompatibilitätsschicht kommen. Alle WIA-Geräte, die die TWAIN-Kompatibilitätsschicht durchlaufen, haben "WIA-" als Präfix, sodass Sie leicht gefiltert werden können.

 

 



