---
description: Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichenfolgen von einem Zeichenfolgentyp in einen anderen.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Übersetzung zwischen Zeichenfolgentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b62ae39307e92c203441ea8ddb9dc61b394a02622e3c86a8949b59539588585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631920"
---
# <a name="translation-between-string-types"></a>Übersetzung zwischen Zeichenfolgentypen

Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichenfolgen von einem Zeichenfolgentyp in einen anderen.



| Funktion                                           | Beschreibung                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Übersetzt eine Zeichenfolge in eine andere.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Karten Zeichenfolge nach Dem-Locale-Zeichen.                      |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Übersetzt einen virtuellen Schlüsselcode in ein Unicode-Zeichen. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Karten multibyte-Zeichenfolge in eine Unicode-Zeichenfolge.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Karten unicode-Zeichenfolge in eine Multibytezeichenfolge.            |



 

Die [**Funktionen WideCharToMultiByte und**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sind besonders nützlich für Anwendungen, die mehrere Zeichenfolgentypen unterstützen. ANSI C definiert auch die **Konvertierungsfunktionen wcstombs** und **mbstowcs**. Sie können jedoch nur in den und aus dem Zeichensatz konvertieren, der von der C-Standardbibliothek unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unicode in der Windows-API](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
