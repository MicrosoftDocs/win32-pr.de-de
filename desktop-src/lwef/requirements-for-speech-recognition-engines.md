---
title: Anforderungen für Spracherkennungs-Engines
description: Anforderungen für Spracherkennungs-Engines
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947967"
---
# <a name="requirements-for-speech-recognition-engines"></a>Anforderungen für Spracherkennungs-Engines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Eine Spracherkennungs-Engine muss auch ein vollständig kompatibles Befehls-und Steuerungs Modul (c&c) gemäß SAPI 4,0 sein. Es muss mehrere Grammatiken in dem Binärformat unterstützen, das in der Spezifikation beschrieben ist, und diese Grammatiken in Echtzeit aktivieren oder deaktivieren.

Beachten Sie, dass SAPI 4,0 erfordert, dass Spracherkennungs-Engines das breit Zeichen, Unicode-Schnittstellen unterstützen. Bei der Unterstützung dieser Schnittstellen sollte die Engine jedoch nicht von der Umstellung von Unicode-Daten in ANSI abhängig sein, da die Engine auf einigen Systemen möglicherweise nicht ordnungsgemäß funktioniert. Beispielsweise funktioniert ein japanisches Modul, das Unicode in ANSI konvertiert, möglicherweise nicht auf einem englischsprachigen Microsoft Windows 95-System.

Damit die Engine als Microsoft-Agent-kompatibel betrachtet wird, muss Sie Ergebnis Objekte zurückgeben, nachdem ein Ausdruck erfolgreich erkannt wurde (über isrgramnotifysinkwh::P hrasefinish). Diese Ergebnis Objekte müssen isrresbasic unterstützen, da die Spezifikation erfordert. Außerdem sollten Sie isrresscore unterstützen. Obwohl der Microsoft-Agent mit einem Modul ausgeführt wird, das nur isrresbasic unterstützt, oder sogar mit einem Modul, das keine Ergebnis Objekte zurückgibt, ist die Leistung in der Regel mit diesen Engines erheblich ärmer. Viele Anwendungen verwenden die von der-Engine bereitgestellten Konfidenz Werte, um zu steuern, wie Sie auf verschiedene Befehle reagieren.

 

 




