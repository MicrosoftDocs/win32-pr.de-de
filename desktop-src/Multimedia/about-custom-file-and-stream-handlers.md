---
title: Informationen zu benutzerdefinierten Datei- und Streamhandlern
description: Informationen zu benutzerdefinierten Datei- und Streamhandlern
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video für Windows (VFW), benutzerdefinierte Dateihandler
- Video für Windows (VFW), benutzerdefinierte Streamhandler
- Video für Windows (VFW), Dateihandler
- Video für Windows (VFW), Streamhandler
- VFW (Video für Windows),benutzerdefinierte Dateihandler
- VFW (Video für Windows),benutzerdefinierte Streamhandler
- VFW (Video für Windows),Dateihandler
- VFW (Video für Windows),Streamhandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719c5312c5ba1e783e0cd4cdb81565f66241e4662772ca441283571f0335fb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145157"
---
# <a name="about-custom-file-and-stream-handlers"></a>Informationen zu benutzerdefinierten Datei- und Streamhandlern

Ihre Anwendung kann einen benutzerdefinierten Dateihandler verwenden, um aus einer Datei zu lesen oder in eine Datei zu schreiben, die in einem nicht standardmäßigen Format vorliegt. Hierzu verwendet Ihre Anwendung beim Öffnen der Datei oder beim Zuordnen der Dateischnittstelle einfach den Namen Ihres Dateihandlers. Die AVIFile-Bibliothek verwendet dann die Funktionen ihres Dateihandlers anstelle der Funktionen eines anderen Dateihandlers. Das nicht standardmäßige Format wird als STANDARD-AVI-Daten für Ihre Anwendung oder eine andere Anwendung mithilfe Ihres benutzerdefinierten Dateihandlers angezeigt.

Auf ähnliche Weise kann Ihre Anwendung einen benutzerdefinierten Streamhandler verwenden, um einen Stream zu lesen, der in einem nicht dem Standard entsprechenden Format vorliegt. Ein Stream – unabhängig davon, ob es sich um Audio-, Video-, CSV-, Text- oder benutzerdefinierte Daten handelt – ist eine Komponente einer AVI-Datei. Beispielsweise besteht eine AVI-Datei, die eine Videosequenz, ein englisches Und-Französisch enthält, aus drei Streams. Ihre Anwendung kann die Streams in einer AVI-Datei angeben, die verarbeitet werden sollen, und jeden dieser Datenströme an einen Handler leiten, der den geeigneten Typ von Multimediadaten optimal verarbeiten kann.

> [!Note]  
> Sie müssen benutzerdefinierte Stream- und Dateihandler in einer oder mehreren DLLs platzieren, die von den Hauptanwendungsdateien getrennt sind.

 

 

 




