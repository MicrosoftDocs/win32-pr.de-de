---
description: Die empfohlene programmgesteuerte Technik zum Festlegen von Kontexten in einer Anwendung, für die keine Ink-Aktivierung aktiviert ist, besteht in der Verwendung der SetInputScope-Funktionen, um den Feldern in der Anwendung Kontext zu zuordnen.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Festlegen des Kontexts mit den SetInputScope-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0abe9992e4a4ee81190fdee022b11f443592e05d7c99f9a5e69d0a200f63ecbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708150"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Festlegen des Kontexts mit den SetInputScope-APIs

Die empfohlene programmgesteuerte Technik zum Festlegen von Kontexten in einer Anwendung, für die keine Ink-Aktivierung aktiviert ist, besteht in der Verwendung der [**SetInputScope-Funktionen,**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) um den Feldern in der Anwendung Kontext zu zuordnen.

Das Microsoft Windows XP Tablet PC Edition Development Kit 1.7 war die erste Version von Microsoft Windows, die [**SetInputScope anbieten konnte.**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) Windows Vista bietet auch Unterstützung für diese Funktionen. Die **SetInputScope-Definitionen** werden in InputScope.idl und InputScope.h deklariert. Weitere Informationen finden Sie unter [Textdienstframework](../tsf/text-services-framework.md).

Die [**SetInputScope-Funktionen**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sind die empfohlene Methode zum Festlegen des Kontexts für Steuerelemente und Anwendungen, die nicht für Ink aktiviert sind.

## <a name="common-input-scopes"></a>Allgemeine Eingabebereich

Mit den [**SetInputScope-Funktionen**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) und dem definierten Satz von allgemeinen Eingabebereich, die in der [**InputScope-Enumeration**](/windows/win32/api/inputscope/ne-inputscope-inputscope) beschrieben werden, können Sie die Erkennungsgenauigkeit der Microsoft-Handschrifterkennungen verbessern.

> [!Note]  
> Die Recognizer für Englisch (USA), Englisch (Vereinigtes Königreich), Deutsch, Französisch, Italienisch, Spanisch, Niederländisch und Portugiesisch unterstützen derzeit die Verwendung der allgemeinen Eingabebereich mit [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
