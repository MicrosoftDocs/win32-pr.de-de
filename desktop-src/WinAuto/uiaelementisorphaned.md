---
title: Uiaelementisorphaned
description: Uiaelementisorphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340213"
---
# <a name="uiaelementisorphaned"></a>Uiaelementisorphaned

## <a name="text"></a>Text

Das Element ist ein verwaistes AutomationElement in der Struktur.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die Adresse der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle des Objekts, die für die angegebenen Koordinaten abgerufen wurde, ist ein Verweis auf ein verwaistes Element in der Elementstruktur.

Dieses Problem ist ein Problem für Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, da Elemente als unsichtbar behandelt werden und dem Benutzer nicht angekündigt werden.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.
-   Eine falsche oder ungültige Implementierung der Benutzeroberflächen Automatisierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuiautomationelement. elementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




