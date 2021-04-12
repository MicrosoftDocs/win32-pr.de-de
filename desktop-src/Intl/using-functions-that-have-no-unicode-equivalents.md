---
description: Funktionen, die nicht mit einer Unicode-Version implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Verwenden von Funktionen, die keine Unicode-Entsprechungen aufweisen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218692"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Verwenden von Funktionen, die keine Unicode-Entsprechungen aufweisen

Funktionen, die nicht mit einer [Unicode](unicode.md) -Version implementiert wurden, wurden in der Regel durch leistungsfähigere oder erweiterte Funktionen ersetzt, die Unicode unterstützen. Wenn Sie z. b. Code portieren, der die [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) -Funktion aufruft, kann die Anwendung Unicode unterstützen, indem Sie stattdessen die Funktion "up [**File**](/windows/win32/api/fileapi/nf-fileapi-createfilea) " verwendet.

Wenn eine Funktion keine Unicode-Entsprechung hat, kann die Anwendung vor und nach dem Funktions aufrufzeichen Zeichen aus 8-Bit-Zeichensätzen zuordnen. Die Zahlen Formatierungsfunktionen " **atoi** " und " **idea** " verwenden z. b. nur die Ziffern 0 bis 9. Die Zuordnung von Unicode zu 8-Bit-Zeichen führt normalerweise zu Datenverlusten. Dies kann jedoch vermieden werden, indem der Codetyp unabhängig voneinander und die Ausdrücke bedingt werden. Die Anweisungen im folgenden Beispiel, die für 8-Bit-Zeichen geschrieben wurden, sind typabhängig und sollten geändert werden, damit Unicode unterstützt wird.


```C++
char str[4] = "137";

int num = atoi(str);
```



Diese Anweisungen können wie folgt umgeschrieben werden, um Sie typunabhängig zu machen.


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



In diesem Beispiel übersetzt die Standard-C-Bibliotheksfunktion **wcstomsb** Unicode in ASCII. Im Beispiel wird davon ausgegangen, dass die Ziffern 0 bis 9 immer aus Unicode in ASCII übersetzt werden können, auch wenn ein Teil des umgebenden Texts nicht möglich ist. Die **atoi** -Funktion hält an jedem Zeichen an, das keine Ziffer ist.

Die Anwendung kann die [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) -Funktion der National Language Support (NLS) verwenden, um Text zu verarbeiten, der die systemeigenen [Ziffern](digit-shapes.md) enthält, die für einige der Skripts in Unicode bereitgestellt werden.

> [!Caution]  
> Wenn Sie die **wcstomsb** -Funktion falsch verwenden, kann die Sicherheit Ihrer Anwendung beeinträchtigt werden. Stellen Sie sicher, dass der Anwendungs Puffer für die Zeichenfolge von 8-Bit-Zeichen mindestens die Größe 2 \* (*Char \_ length* + 1) hat, wobei *Char \_ length* die Länge der Unicode-Zeichenfolge darstellt. Diese Einschränkung wird vorgenommen, da jedes Unicode-Zeichen mit [Doppelbyte-Zeichensätzen (Double-Byte Character Sets](double-byte-character-sets.md) , dbcss) zwei aufeinander folgenden 8-Bit-Zeichen zugeordnet werden kann. Wenn der Puffer nicht die gesamte Zeichenfolge enthält, wird die Ergebnis Zeichenfolge nicht mit Null beendet und stellt ein Sicherheitsrisiko dar. Weitere Informationen zur Anwendungssicherheit finden Sie unter [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
