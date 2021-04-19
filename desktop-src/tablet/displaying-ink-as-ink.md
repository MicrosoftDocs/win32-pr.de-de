---
description: Das Standardverhalten für das InkEdit-Steuerelement besteht darin, frei Hand Eingaben zu erkennen und in Text zu konvertieren, nachdem ein kurzes Timeout abgelaufen ist.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Anzeigen von frei Hand Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349627"
---
# <a name="displaying-ink-as-ink"></a>Anzeigen von frei Hand Eingaben

Das Standardverhalten für das [InkEdit](inkedit-control-reference.md) -Steuerelement besteht darin, frei Hand Eingaben zu erkennen und in Text zu konvertieren, nachdem ein kurzes Timeout abgelaufen ist. Da es sich bei dem Steuerelement um eine übergeordnete Klasse von [RichEdit](../controls/rich-edit-controls.md)handelt, ist es auch möglich, frei Hand Eingaben im Steuerelement einzubetten und anzuzeigen. Jedes Wort wird als [**InkDisp**](inkdisp-class.md) -Objekt in das-Steuerelement eingefügt. Das **InkDisp** -Objekt enthält die frei Hand Eingaben und deren Erkennungs Alternativen.

Beim Einfügen wird die frei Hand Eingabe auf den aktuellen Schrift Grad skaliert, und andere Umgebungs Eigenschaften, z. b. kursiv oder Fett, werden angewendet. Wenn der Benutzer den Text eines [**InkDisp**](inkdisp-class.md) -Objekts bearbeitet, muss er zuerst die frei Hand Eingaben in Text konvertieren.

> [!Note]  
> Alle alternativen Freihand-und Erkennungs Daten gehen während der Konvertierung verloren.

 

Diese Funktion ist nur auf Computern verfügbar, auf denen Microsoft Windows XP Tablet PC Edition, Windows Vista oder höher ausgeführt wird.

 

 
