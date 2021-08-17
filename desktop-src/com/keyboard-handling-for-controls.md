---
title: Tastaturbehandlung für Steuerelemente
description: Ein Steuerelement reagiert auf Tastenkombinationen, damit der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26081d36c62b11163ceb8c41421ea0370d18b3ce9bf16be68e4e8a06a5f1a489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736557"
---
# <a name="keyboard-handling-for-controls"></a>Tastaturbehandlung für Steuerelemente

Ein Steuerelement reagiert auf Tastenkombinationen, damit der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden. Der Container verwaltet die Tastaturaktivität für alle eingebetteten Steuerelemente. Bei Verbunddokumenten gelten Tastenkombinationen nur für das derzeit aktive Objekt. Mit -Steuerelementen wurde ein Mechanismus hinzugefügt, damit ein Steuerelement auf seine Tastatur-Mnemonie reagieren kann, auch wenn es derzeit nicht auf der Benutzeroberfläche aktiv ist.

Die [**Methoden IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) und [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) und [**die IOleControlSite::OnControlInfoChanged-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) verarbeiten die mnemonischen Tastaturen eines Steuerelements. Eine [**CONTROLINFO-Struktur**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) beschreibt die mnemonischen Zugriffstasten eines Steuerelements, und die Flags, die mit der **GetControlInfo-Methode** zurückübergaben, beschreiben das Verhalten der Steuerelemente mit den Tasten ENTER und ESC. Wenn ein Steuerelement seine mnemonischen Daten ändert, ruft es **OnControlInfoChanged** auf, damit der Container die Struktur bei Bedarf erneut laden kann.

Wenn ein Steuerelement auf der Benutzeroberfläche aktiv ist, ist es auch das Steuerelement mit dem Fokus. Wenn Steuerelemente zwischen den aktiven und aktiven Benutzeroberflächenzuständen aktiviert und deaktiviert werden, ruft das Steuerelement [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) auf, um den Container über solche Änderungen zu informieren.

Wenn ein Steuerelement auf der Benutzeroberfläche aktiv ist, hat es außerdem die erste Möglichkeit, Tastatureingaben zu verarbeiten. Um einem Container die Möglichkeit zu geben, die Tastatureingabe vor dem Steuerelement zu verarbeiten, ruft das Steuerelement [**IOleControlSite::TranslateAccelerator auf.**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator) Wenn der Container die Tastatureingabe nicht verarbeitet, verarbeitet das Steuerelement diese.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




