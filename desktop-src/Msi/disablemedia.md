---
description: Wenn diese System Richtlinie pro Benutzer auf &\# 0034; 1&0034; festgelegt ist \# , können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: Disablemedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961092"
---
# <a name="disablemedia"></a>Disablemedia

Wenn diese [System Richtlinie](system-policy.md) pro Benutzer auf "1" festgelegt ist, können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden. Das Durchsuchen anderer Produkte wird verhindert, unabhängig davon, ob die Installation mit erweiterten Berechtigungen erfolgt. Der Benutzer kann das Produkt weiterhin von einem Medium aus neu installieren, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die [**disablemedia**](-disablemedia.md) -Eigenschaft eine andere Auswirkung hat als die disablemedia-Richtlinie. Wenn Sie die System Richtlinie "disablemedia" festlegen, wird nur das Durchsuchen von Medienquellen deaktiviert. Durch Festlegen der **disablemedia** -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 



