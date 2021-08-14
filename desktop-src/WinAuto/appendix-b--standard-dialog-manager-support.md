---
title: Anhang B– Unterstützung für Standarddialog-Manager
description: Microsoft Active Accessibility bietet vollständige Unterstützung für DIALOGFELD-Steuerelemente im Standarddialog-Manager (Standard Dialog Manager, SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b6500cabf4820fffe12b7ef160f2e494e43db067f6b96409dee02bbfd6119e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326821"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Anhang B: Unterstützung des Standarddialog-Managers

Microsoft Active Accessibility bietet vollständige Unterstützung für DIALOGFELD-Steuerelemente im Standarddialog-Manager (Standard Dialog Manager, SDM). SDM ist eine interne Microsoft-Codebibliothek, die Microsoft-Anwendungen ein gewisses Maß an Abhängigkeit von den Unterschieden zwischen macintosh- und microsoft Windows bietet. SDM wird hauptsächlich für Dialogfelder in Microsoft Excel und Microsoft Word.

SDM stellt Probleme bei Barrierefreiheitshilfen vor, da nicht standardmäßige Implementierungen von Dialogfeldern verwendet werden. Beispielsweise verwenden SDM-Dialogfeldschaltflächen fensterhandles nicht auf die gleiche Weise wie die Standardelemente der Benutzeroberfläche. Sie können keine Nachrichten an Schaltflächen senden, und Schaltflächen sind nicht in der Fensterliste enthalten. Eine Anwendung, die SDM verwendet, kommuniziert über eine private Schnittstelle mit dem Steuerelement.

Die folgende Abbildung zeigt ein Beispieldialogfeld aus Word. Obwohl es wie ein reguläres Windows, das das Registerkarten-Steuerelement verwendet, ist es tatsächlich ein SDM-Dialogfeld.

![Screenshot des Dialogfelds "Optionen" mit ausgewählter Registerkarte "Ansicht"](images/dialog.gif)

 

 




