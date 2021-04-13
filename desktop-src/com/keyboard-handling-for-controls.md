---
title: Tastatur Behandlung für Steuerelemente
description: Ein-Steuerelement reagiert auf Tastaturbeschleuniger, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311400"
---
# <a name="keyboard-handling-for-controls"></a>Tastatur Behandlung für Steuerelemente

Ein-Steuerelement reagiert auf Tastaturbeschleuniger, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden. Der Container verwaltet die Tastatur Aktivität für alle eingebetteten Steuerelemente. Mit Verbund Dokumenten gelten die Tastaturbeschleuniger nur für das derzeit aktive Objekt. Mit-Steuerelementen wurde ein Mechanismus hinzugefügt, sodass ein Steuerelement auf seine Tastatur-mnetmonics reagieren kann, auch wenn es zurzeit nicht auf der Benutzeroberfläche aktiv ist.

Die [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) -und [**IOleControl:: onmnetmonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) -Methoden und die [**iolecontrolsite:: oncontrolinfochanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) -Methode behandeln die Tastatur-mnetmonics eines Steuer Elements. Eine [**controlInfo**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) -Struktur beschreibt die mnetmonischen Accelerators eines Steuer Elements, und die zurückgegebenen Flags über die **GetControlInfo** -Methode beschreiben das Verhalten der Steuerelemente mit der EINGABETASTE und der ESC-Taste. Wenn ein Steuerelement seine mnetmonics ändert, ruft es **oncontrolinfochanged** auf, damit der Container die Struktur bei Bedarf erneut laden kann.

Wenn ein Steuerelement aktiv ist, ist es auch das Steuerelement mit dem Fokus. Beim Aktivieren und Deaktivieren von Steuerelementen zwischen den direkten aktiven und den aktiven UI-Zuständen Ruft das Steuerelement [**iolecontrolsite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) auf, um den Container über solche Änderungen zu informieren.

Wenn ein Steuerelement aktiv ist, hat es außerdem die Möglichkeit, beliebige Tastatureingaben zu verarbeiten. Um einem Container die Möglichkeit zu geben, die Tastatureingabe vor dem Steuerelement zu verarbeiten, ruft das Steuerelement [**iolecontrolsite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)auf. Wenn der Container die Tastatureingabe nicht behandelt, wird er vom-Steuerelement verarbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




