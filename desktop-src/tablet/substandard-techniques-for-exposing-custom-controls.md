---
description: Beschreibung der nicht standardmäßigen Techniken zum Verfügbarmachen benutzerdefinierter Steuerelemente.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Nicht standardmäßige Techniken zum Verfügbarmachen von benutzerdefinierten Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121856bf5303b011b785a26bc47013e0df93463d7f278d6e4586991a47d8e020
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934310"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Nicht standardmäßige Techniken zum Verfügbarmachen von benutzerdefinierten Steuerelementen

Wenn eine Anwendung Microsoft Active Accessibility nicht unterstützt, ist sie möglicherweise nicht vollständig zugänglich. Mit den folgenden Techniken werden Steuerelemente teilweise kompatibel gerendert:

-   Gibt eine beschreibende Zeichenfolge zurück, wenn das Steuerelement mithilfe der WM \_ GETTEXT-Nachricht abgefragt wird. Lassen Sie beispielsweise zu, dass eine benutzerdefinierte Entsprechung eines Schaltflächensteuerelements mit der Bezeichnung "Drucken" die Zeichenfolge "Schaltfläche drucken" zurückgibt. Dadurch werden sowohl der Steuerelementtyp als auch die Bezeichnung identifiziert. Dieselbe Zeichenfolge eignet sich für eine Schaltfläche mit einer Bezeichnung, die etwas anderes als Text ist, z. B. eine Grafik eines Druckers. Lassen Sie auf ähnliche Weise zu, dass ein benutzerdefiniertes Steuerelement, das sich wie ein Kontrollkästchen verhält, die Beschriftungszeichenfolge "Druck aktiviert, aktiviert" zurückgibt.
-   Unterstützen Sie die WM \_ GETDLGCODE-Nachricht, um die unterstützte Tastatureingabe zu identifizieren. Lassen Sie beispielsweise zu, dass ein benutzerdefiniertes Äquivalent eines Bearbeitungssteuerelements WM \_ GETDLGCODE behandelt, indem Sie DLGC \_ HASSETSEL zurückgeben, wenn nachrichten verarbeitet werden, um die Auswahl festzulegen, DLGC \_ WANTWS, wenn Pfeiltasten verwendet werden, und DLGC \_ WANTCHARS, um anzugeben, dass die Zeicheneingabe verwendet wird.
    > [!Note]  
    > Nur Steuerelemente, die über eigene Fensterhandles verfügen, können auf die WM \_ GETTEXT- und WM \_ GETDLGCODE-Meldungen reagieren.

     

Um Kompatibilitätsprobleme mit Barrierefreiheitshilfen zu vermeiden, sollten Sie beim Entwerfen benutzerdefinierter Steuerelemente Active Accessibility Richtlinien genau befolgen. Weitere Informationen zum Vermeiden von Kompatibilitätsproblemen mit Barrierefreiheitshilfen finden Sie im Abschnitt [Barrierefreiheit.](../accessibility/accessibility.md)

 

 
