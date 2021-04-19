---
description: Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichen folgen aus einem Zeichen folgertyp in einen anderen.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Übersetzung zwischen Zeichen folgen Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349442"
---
# <a name="translation-between-string-types"></a>Übersetzung zwischen Zeichen folgen Typen

Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichen folgen aus einem Zeichen folgertyp in einen anderen.



| Funktion                                           | BESCHREIBUNG                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Übersetzt eine Zeichenfolge in eine andere Zeichenfolge.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Ordnet eine Zeichenfolge nach dem Gebiets Schema zu.                      |
| [**Zu Unicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Übersetzt einen virtuellen Schlüsselcode in ein Unicode-Zeichen. |
| [**MultiByteToWideChar muss**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Ordnet eine Multibytezeichenfolge einer Unicode-Zeichenfolge zu.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Ordnet eine Unicode-Zeichenfolge einer Multibytezeichenfolge zu.            |



 

Die Funktionen [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) und [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sind besonders nützlich für Anwendungen, die mehrere Zeichen folgen Typen unterstützen. ANSI C definiert auch die Konvertierungs Funktionen **wcstomb** und **mbstowcs**, aber Sie können nur in den und aus dem von der Standard-C-Bibliothek unterstützten Zeichensatz konvertieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
