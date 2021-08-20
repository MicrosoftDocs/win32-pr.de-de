---
description: Wenn diese Benutzersystemrichtlinie auf &\# 0034;1&\# 0034; festgelegt ist, können Benutzer und Administratoren, die eine Wartungsinstallation eines Produkts ausführen, das Dialogfeld Durchsuchen nicht verwenden, um Medienquellen wie CD-ROM für die Quellen anderer installierbarer Produkte zu durchsuchen.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143246"
---
# <a name="disablemedia"></a>DisableMedia

Wenn diese [Systemrichtlinie](system-policy.md) pro Benutzer auf "1" festgelegt ist, werden Benutzer und Administratoren, die eine Wartungsinstallation eines Produkts ausführen, daran gehindert, das Dialogfeld Durchsuchen zum Durchsuchen von Medienquellen wie CD-ROM für die Quellen anderer installierbarer Produkte zu verwenden. Das Suchen nach anderen Produkten wird unabhängig davon verhindert, ob die Installation mit erhöhten Rechten erfolgt. Es ist weiterhin möglich, dass der Benutzer das Produkt über Medien neu installiert, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

Beachten Sie, dass die [**DISABLEMEDIA-Eigenschaft**](-disablemedia.md) eine andere Auswirkung als die DisableMedia-Richtlinie hat. Wenn Sie die Systemrichtlinie DisableMedia festlegen, wird nur das Navigieren zu Medienquellen deaktiviert. Durch Festlegen der **DISABLEMEDIA-Eigenschaft** wird verhindert, dass das Installationsprogramm Medienquellen wie cd-ROM als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen jedoch aktiviert ist, kann ein Benutzer weiterhin zu einer Medienquelle navigieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 



