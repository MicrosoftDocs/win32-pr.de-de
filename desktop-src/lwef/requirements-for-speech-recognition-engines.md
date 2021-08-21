---
title: Anforderungen für Spracherkennungs-Engines
description: Anforderungen für Spracherkennungs-Engines
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975750"
---
# <a name="requirements-for-speech-recognition-engines"></a>Anforderungen für Spracherkennungs-Engines

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Eine Spracherkennungs-Engine muss auch eine vollständig konforme Command & Control-Engine (C&amp;C) gemäß SAPI 4.0 sein. Sie muss mehrere Grammatiken im binären Format unterstützen, das in der Spezifikation beschrieben wird, und diese Grammatiken in Echtzeit aktivieren oder deaktivieren können.

Beachten Sie, dass SAPI 4.0 erfordert, dass Spracherkennungs-Engines die Unicode-Schnittstellen für Breitzeichen unterstützen. Bei der Unterstützung dieser Schnittstellen sollte die Engine jedoch nicht von der Konvertierung von Unicode-Daten in ANSI abhängig sein, da die Engine auf einigen Systemen möglicherweise nicht ordnungsgemäß funktioniert. Beispielsweise funktioniert eine japanische Engine, die Unicode in ANSI konvertiert, möglicherweise nicht auf einem englischsprachigen Microsoft Windows 95-System.

Darüber hinaus muss die Engine bei erfolgreicher Erkennung eines Ausdrucks (über ISRGramNotifySinkW::P hraseFinish) Ergebnisobjekte zurückgeben, um als Microsoft Agent-kompatibel angesehen zu werden. Diese Ergebnisobjekte müssen ISRResBasic unterstützen, wie es die Spezifikation erfordert. Darüber hinaus sollten sie ISRResScore unterstützen. Obwohl Microsoft Agent mit einer Engine ausgeführt wird, die nur ISRResBasic unterstützt, oder sogar mit einer Engine, die keine Ergebnisobjekte zurückgibt, ist die Leistung bei solchen Engines in der Regel deutlich schlechter. Viele Anwendungen verwenden die von der Engine bereitgestellten Konfidenzwerte, um zu steuern, wie sie auf verschiedene Befehle reagieren.

 

 




