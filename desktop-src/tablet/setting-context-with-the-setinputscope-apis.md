---
description: Die empfohlene programmgesteuerte Methode zum Festlegen von Kontexten in einer Anwendung, die nicht frei Hand fähig ist, besteht darin, die SetInputScope-Funktionen zu verwenden, um den Feldern in der Anwendung Kontext zuzuordnen.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Festlegen des Kontexts mit den "*"-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350298"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Festlegen des Kontexts mit den "*"-APIs

Die empfohlene programmgesteuerte Methode zum Festlegen von Kontexten in einer Anwendung, die nicht frei Hand fähig ist, besteht darin, die [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen zu verwenden, um den Feldern in der Anwendung Kontext zuzuordnen.

Das Microsoft Windows XP Tablet PC Edition Development Kit 1,7 war die erste Version von Microsoft Windows für die Bereitstellung von " [**stinputscope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)". Windows Vista bietet auch Unterstützung für diese Funktionen. Die **Definitionen** von "*" werden in "InputScope. idl" und "InputScope. h" deklariert. Weitere Informationen finden Sie unter [Text Services-Framework](../tsf/text-services-framework.md).

Die [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen sind die empfohlene Methode, um Kontext für Steuerelemente und Anwendungen festzulegen, für die keine frei Hand Eingabe aktiviert ist.

## <a name="common-input-scopes"></a>Allgemeine Eingabe Bereiche

Mithilfe der [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -Funktionen und der definierten Gruppe allgemeiner Eingabe Bereiche, die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration beschrieben werden, können Sie die Erkennungsgenauigkeit der Handschrift Erkennungsfunktionen von Microsoft verbessern.

> [!Note]  
> Die Erkennungs Tools für Englisch (USA), Englisch (Vereinigtes Königreich), Deutsch, Französisch, Italienisch, Spanisch, Niederländisch und Portugiesisch unterstützen derzeit die Verwendung der allgemeinen Eingabe Bereiche mit "* [**tinputscope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)".

 

 

 
