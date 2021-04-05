---
title: Anhang B-Unterstützung für Standard Dialogfelder
description: Microsoft Active Accessibility bietet umfassende Unterstützung für SDM-Dialogfeld-Steuerelemente (Standard Dialogfeld-Manager).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710866"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Anhang B: Unterstützung von Standard Dialog-Manager

Microsoft Active Accessibility bietet umfassende Unterstützung für SDM-Dialogfeld-Steuerelemente (Standard Dialogfeld-Manager). SDM ist eine interne Microsoft-Code Bibliothek, mit der Microsoft-Anwendungen ein gewisses Maß an Unabhängigkeit von den Unterschieden zwischen Macintosh-und Microsoft Windows-Betriebssystemen bereitgestellt werden. SDM wird hauptsächlich für Dialogfelder in Microsoft Excel und Microsoft Word verwendet.

SDM stellt Probleme für Barrierefreiheits Hilfen dar, da es nicht standardmäßige Implementierungen von Dialogfeldern verwendet. Beispielsweise verwenden SDM-Dialogfeld Schaltflächen keine Fenster Handles auf die gleiche Weise wie die standardmäßigen Benutzeroberflächen Elemente. Sie können keine Nachrichten an Schaltflächen senden, und Schaltflächen sind nicht in der Fensterliste enthalten. Eine Anwendung, die SDM verwendet, kommuniziert über eine private Schnittstelle mit dem-Steuerelement.

Die folgende Abbildung zeigt ein Beispiel Dialogfeld aus Word. Obwohl es sich um ein normales Windows-Dialogfeld handelt, das das Registerkarten-Steuerelement verwendet, handelt es sich tatsächlich um ein SDM-Dialogfeld.

![Screenshot des Dialog Felds "Optionen" mit ausgewählter Registerkarte "Ansicht"](images/dialog.gif)

 

 




