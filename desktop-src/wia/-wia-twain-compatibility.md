---
description: WIA bietet eine TWAIN-Kompatibilitätsebene, mit der TWAIN-orientierte Anwendungen mit WIA-Geräten (Windows Image Acquisition) kommunizieren können.
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: TWAIN-Kompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056980"
---
# <a name="twain-compatibility"></a>TWAIN-Kompatibilität

WIA bietet eine TWAIN-Kompatibilitätsebene, mit der TWAIN-orientierte Anwendungen mit WIA-Geräten (Windows Image Acquisition) kommunizieren können. TWAIN-orientierte Anwendungen haben keinen Vollzugriff auf WIA-Funktionen. Beispielsweise kann eine Anwendung die Benutzeroberfläche nicht mithilfe der TWAIN-Kompatibilitätsebene unterdrücken.

WIA-Geräte werden zweimal für eine Anwendung angezeigt, die WIA und TWAIN kennt: einmal über die normale WIA-Kommunikation und einmal über die TWAIN-Kompatibilitätsebene. Um zu vermeiden, dass ein WIA-Gerät zweimal auflistet, muss eine Anwendung, die sowohl WIA als auch TWAIN kennt, die WIA-Geräte herausfiltern, die über die TWAIN-Kompatibilitätsebene kommen. Alle WIA-Geräte, die die TWAIN-Kompatibilitätsebene verwenden, verfügen über "WIA-" als Präfix, sodass sie leicht gefiltert werden können.

 

 



