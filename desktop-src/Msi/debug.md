---
description: Wenn diese computerspezifische Systemrichtlinie auf &\# 0034;1&0034; festgelegt ist, schreibt das Installationsprogramm allgemeine Debugmeldungen mithilfe der \# OutputDebugString-Funktion in den Debugger.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692870"
---
# <a name="debug"></a>Debug

Wenn diese computerspezifische [Systemrichtlinie](system-policy.md) auf "1" festgelegt ist, schreibt das Installationsprogramm allgemeine Debugmeldungen mithilfe der [**OutputDebugString-Funktion**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) in den Debugger. Wenn dieser Wert auf "2" festgelegt ist, schreibt das Installationsprogramm alle gültigen Debugmeldungen mithilfe der [**OutputDebugString-Funktion in den**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Debugger. Diese Richtlinie dient nur zu Debugzwecken und wird in zukünftigen Versionen des Windows möglicherweise nicht unterstützt.

Windows Das Installationsprogramm schreibt Befehlszeilen nur dann in die Protokolldatei, wenn das dritte Bit (0x04) im Wert der Debugrichtlinie festgelegt ist. Legen Sie daher den Wert der Debugrichtlinie auf 7 fest, um Befehlszeilen im Protokoll anzuzeigen. Dadurch werden keine Eigenschaften angezeigt, die einem [Steuerelement zum Bearbeiten mit](edit-control.md) dem [Kennwortsteuerungsattribut zugeordnet sind.](password-control-attribute.md) Dadurch werden die in der Befehlszeile festgelegten Eigenschaften auch dann im Protokoll sichtbar, wenn die Eigenschaft in der [**MsiHiddenProperties-Eigenschaft enthalten**](msihiddenproperties.md) ist. Weitere Informationen finden Sie unter [Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 
