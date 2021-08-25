---
description: Funktionen, die nicht mit einer Unicode-Version implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Verwenden von Funktionen ohne Unicode-Entsprechungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787880"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Verwenden von Funktionen ohne Unicode-Entsprechungen

Funktionen, die nicht mit einer [Unicode-Version](unicode.md) implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen. Wenn Sie beispielsweise Code portieren, der die [**OpenFile-Funktion**](/windows/win32/api/winbase/nf-winbase-openfile) aufruft, kann Ihre Anwendung Unicode mithilfe der [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) unterstützen.

Wenn eine Funktion über kein Unicode-Äquivalent verfügt, kann die Anwendung Zeichen vor und nach dem Funktionsaufruf 8-Bit-Zeichensätzen zuordnen. Beispielsweise verwenden die Zahlenformatierungsfunktionen **atoi** und **itoa** nur die Ziffern 0 bis 9. Normalerweise führt die Zuordnung von Unicode zu 8-Bit-Zeichen zu Datenverlusten. Dies kann jedoch vermieden werden, indem der Code typunabhängig und die Ausdrücke bedingt werden. Die Anweisungen im folgenden Beispiel, die für 8-Bit-Zeichen geschrieben wurden, sind typabhängig und sollten geändert werden, um Unicode zu unterstützen.


```C++
char str[4] = "137";

int num = atoi(str);
```



Diese Anweisungen können wie folgt umgeschrieben werden, um sie typunabhängig zu machen.


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



In diesem Beispiel übersetzt die C-Standardbibliotheksfunktion **wcstombs** Unicode in ASCII. Das Beispiel basiert auf der Tatsache, dass die Ziffern 0 bis 9 immer aus Unicode in ASCII übersetzt werden können, auch wenn ein Teil des umgebenden Texts dies nicht kann. Die **atoi-Funktion** wird bei jedem Zeichen angehalten, das keine Ziffer ist.

Ihre Anwendung kann die [**LCMapString-Funktion**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) (National Language Support, NLS) verwenden, um Text zu verarbeiten, der die nativen Ziffern enthält, die für einige der [Skripts](digit-shapes.md) in Unicode bereitgestellt werden.

> [!Caution]  
> Die fehlerhafte **Verwendung der wcstombs-Funktion** kann die Sicherheit Ihrer Anwendung gefährden. Stellen Sie sicher, dass der Anwendungspuffer für die Zeichenfolge mit 8-Bit-Zeichen mindestens die Größe 2 \* *(Char-Länge \_* +1) hat, wobei *char \_ length* die Länge der Unicode-Zeichenfolge darstellt. Diese Einschränkung wird vorgenommen, da bei [Doppel-Byte-Zeichensätzen](double-byte-character-sets.md) (DBCSs) jedes Unicode-Zeichen zwei aufeinander folgenden 8-Bit-Zeichen zugeordnet werden kann. Wenn der Puffer nicht die gesamte Zeichenfolge enthält, wird die Ergebniszeichenfolge nicht mit NULL beendet, was ein Sicherheitsrisiko bedeutet. Weitere Informationen zur Anwendungssicherheit finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
