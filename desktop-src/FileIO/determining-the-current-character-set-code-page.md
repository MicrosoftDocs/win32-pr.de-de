---
description: Die AreFileApisANSI-Funktion bestimmt, ob die Datei-E/A-Funktionen die Codepage ANSI oder OEM-Zeichensatz verwenden.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Bestimmen der aktuellen Zeichensatz-Codepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150657"
---
# <a name="determining-the-current-character-set-code-page"></a>Bestimmen der aktuellen Zeichensatz-Codepage

Die [**AreFileApisANSI-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) bestimmt, ob die Datei-E/A-Funktionen die Codepage ANSI oder OEM-Zeichensatz verwenden. Die [**SetFileApisToANSI-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) bewirkt, dass die Funktionen die ANSI-Codepage verwenden. Die [**SetFileApisToOEM-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) bewirkt, dass die Funktionen die OEM-Codepage verwenden.

Standardmäßig verwenden Datei-E/A-Funktionen ANSI-Dateinamen. Von Kernel32.dll exportierte Funktionen, die Dateinamen akzeptieren oder zurückgeben, sind von der Einstellung der Dateicodepage betroffen.

Sowohl [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) als auch [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) legen die Codepage pro Prozess und nicht pro Thread oder Computer fest.

 

 



