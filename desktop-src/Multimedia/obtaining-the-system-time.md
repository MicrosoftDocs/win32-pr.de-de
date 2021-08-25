---
title: Abrufen der Systemzeit
description: Abrufen der Systemzeit
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Multimedia-Timer, Systemzeit
- Timer, Systemzeit
- Systemuhrzeit
- timeGetTime-Funktion
- timeGetSystemTime-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806470"
---
# <a name="obtaining-the-system-time"></a>Abrufen der Systemzeit

In der Regel wird die aktuelle Systemzeit abgerufen, bevor eine Anwendung mit der Verwendung der *Multimediazeitdienste beginnt.* Die Systemzeit ist die Zeit in Millisekunden, die seit dem Start des Microsoft Windows Betriebssystems liegt. Sie können die [**TimeGetTime- oder**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) [**timeGetSystemTime-Funktion**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) verwenden, um die Systemzeit abzurufen. Diese beiden Funktionen sind sehr ähnlich: **timeGetTime** gibt die Systemzeit zurück, und **timeGetSystemTime** füllt eine [**MMTIME-Struktur**](/previous-versions//dd757347(v=vs.85)) mit der Systemzeit auf.

 

 