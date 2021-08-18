---
description: Das Standardverhalten für das InkEdit-Steuerelement ist das Erkennen und Konvertieren von Ink in Text, nachdem ein kurzes Timeout abgelaufen ist.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Anzeigen von Ink als Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de038df5c1b7e43f90ea02edc166039d606fe56761c96a47508714fd94ed6530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709470"
---
# <a name="displaying-ink-as-ink"></a>Anzeigen von Ink als Ink

Das Standardverhalten für das [InkEdit-Steuerelement](inkedit-control-reference.md) ist das Erkennen und Konvertieren von Ink in Text, nachdem ein kurzes Timeout abgelaufen ist. Da das Steuerelement eine Oberklasse von [RichEdit](../controls/rich-edit-controls.md)ist, ist es auch möglich, Ink innerhalb des Steuerelements einbetten und anzuzeigen. Jedes Wort wird als [**InkDisp-Objekt in**](inkdisp-class.md) das Steuerelement eingefügt. Das **InkDisp-Objekt** enthält die Ink-Objekte und ihre Erkennungswechsel.

Beim Einfügen wird die Ink-Eigenschaft auf den aktuellen Schriftgrad skaliert, und andere Umgebungseigenschaften, z. B. italisch oder fett, werden angewendet. Wenn sich der Benutzer dafür entscheidet, den Text eines [**InkDisp-Objekts**](inkdisp-class.md) zu bearbeiten, muss er zuerst die Freiform in Text konvertieren.

> [!Note]  
> Während der Konvertierung gehen alle alternativen Daten der Ink- und Erkennung verloren.

 

Dieses Feature ist nur auf Computern verfügbar, auf denen Microsoft Windows XP Tablet PC Edition, Windows Vista oder höher ausgeführt wird.

 

 
