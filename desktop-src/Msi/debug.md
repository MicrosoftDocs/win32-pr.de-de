---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , schreibt der Installer gängige Debugmeldungen mithilfe der OutputDebugString-Funktion in den Debugger.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866363"
---
# <a name="debug"></a>Debuggen

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, schreibt der Installer gängige Debugmeldungen mithilfe der [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) -Funktion in den Debugger. Wenn dieser Wert auf "2" festgelegt ist, schreibt das Installationsprogramm mit der [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) -Funktion alle gültigen Debugmeldungen in den Debugger. Diese Richtlinie dient nur zu Debuggingzwecken und wird in zukünftigen Versionen von Windows Installer möglicherweise nicht mehr unterstützt.

Windows Installer schreibt Befehlszeilen nur in die Protokolldatei, wenn das dritte (0x04) Bit im Wert der debugrichtlinie festgelegt ist. Um Befehlszeilen im Protokoll anzuzeigen, legen Sie den Wert der Debug-Richtlinie daher auf 7 fest. Dadurch werden keine Eigenschaften angezeigt, die einem [Bearbeitungs Steuer](edit-control.md) Element zugeordnet sind, das über das Kenn [Wort Steuerungs Attribut](password-control-attribute.md)verfügt. Dadurch werden die Eigenschaften, die in der Befehlszeile angezeigt werden, im Protokoll angezeigt, auch wenn die Eigenschaft in der [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft enthalten ist. Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 
