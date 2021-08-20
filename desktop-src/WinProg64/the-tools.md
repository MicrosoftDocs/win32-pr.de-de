---
title: Die Tools
description: In diesem Thema werden die Tools beschrieben, die Sie verwenden können, um Ihre Anwendung 64-Bit bereit zu machen. Windows 10 ist sowohl für x64- als auch arm64-basierte Prozessoren verfügbar.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows Programmierung, Tools
- Tools 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28084c445d664e130a9bb6dc5c087f8421cdaa5746845308258662739ee9084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569890"
---
# <a name="the-tools"></a>Die Tools

In diesem Thema werden die Tools beschrieben, die Sie verwenden können, um Ihre Anwendung 64-Bit bereit zu machen. Windows 10 ist sowohl für x64- als auch arm64-basierte Prozessoren verfügbar.

## <a name="include-files"></a>Includedateien

Die API-Elemente sind zwischen 32- und 64-Bit-Windows praktisch identisch. Die Windows Headerdateien wurden so geändert, dass sie sowohl für 32- als auch für 64-Bit-Code verwendet werden können. Die neuen 64-Bit-Typen und -Makros werden in der neuen Headerdatei Basetsd.h definiert, die sich im Satz von Headerdateien befindet, die in Windows.h enthalten sind. Basetsd.h enthält die neuen Datentypdefinitionen, mit deren Hilfe die Wortgröße des Quellcodes unabhängig gemacht werden kann.

## <a name="new-data-types"></a>Neue Datentypen

Die Windows Headerdateien enthalten neue Datentypen. Diese Typen dienen in erster Linie der Typkompatibilität mit den 32-Bit-Datentypen. Die neuen Typen bieten genau die gleiche Typisierung wie die vorhandenen Typen und bieten gleichzeitig Unterstützung für die 64-Bit-Windows. Weitere Informationen finden Sie unter [Die neuen Datentypen](the-new-data-types.md) oder die Basetsd.h-Headerdatei.

## <a name="predefined-macros"></a>Vordefinierte Makros

Der Compiler definiert die folgenden Makros, um die Plattform zu identifizieren.



| Makro   | Bedeutung                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Eine 64-Bit-Plattform. Dies schließt sowohl x64 als auch ARM64 ein.                                                        |
| \_WIN32 | Eine 32-Bit-Plattform. Dieser Wert wird aus Gründen der Abwärtskompatibilität auch vom 64-Bit-Compiler definiert.<br/> |
| \_WIN16 | Eine 16-Bit-Plattform                                                                                           |



 

Die folgenden Makros sind spezifisch für die Architektur.



| Makro      | Bedeutung                |
|------------|------------------------|
| \_M \_ IA64  | Intel Itanium-Plattform |
| \_M \_ IX86  | x86-Plattform           |
| \_M \_ X64   | x64-Plattform           |
| \_M \_ ARM64 | ARM64-Plattform         |



 

Verwenden Sie diese Makros nur mit architekturspezifischem Code, sondern verwenden Sie nach \_ Möglichkeit WIN64, \_ WIN32 und \_ WIN16.

## <a name="helper-functions"></a>Hilfsfunktionen

Die folgenden Inlinefunktionen (definiert in Basetsd.h) können Ihnen helfen, Werte von einem Typ in einen anderen sicher zu konvertieren.

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> **IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.

 

## <a name="64-bit-compiler"></a>64-Bit-Compiler

Die 64-Bit-Compiler können verwendet werden, um Zeigerkürzungen, fehlerhafte Typcasts und andere 64-Bit-spezifische Probleme zu identifizieren.

Wenn der Compiler zum ersten Mal ausgeführt wird, generiert er wahrscheinlich viele Warnungen zum Abschneiden von Zeigern oder Typkonflikten, z. B.:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Verwenden Sie diese Warnungen als Leitfaden, um den Code stabiler zu machen. Es empfiehlt sich, alle Warnungen auszuschließen, insbesondere Warnungen zum Abschneiden von Zeigern.

## <a name="64-bit-compiler-switches-and-warnings"></a>64-Bit-Compilerschalter und -Warnungen

Beachten Sie, dass dieser Compiler das LLP64-Datenmodell aktiviert.

Es gibt eine Warnungsoption zur Unterstützung der Portierung zu LLP64. Der Schalter -Wp64 -W3 aktiviert die folgenden Warnungen:

-   C4305: Kürzungswarnung. Beispiel: "return": Kürzung von "unsigned int64" auf "long".
-   C4311: Abschneidewarnung. Beispiel: "typ cast": Zeigerkürzung von "int \* \_ ptr64" auf "int".
-   C4312: Konvertierung in eine Größere-Größe-Warnung. Beispiel: "Typumwandlung": Konvertierung von "int" in "int \* \_ ptr64" mit größerer Größe.
-   C4318: Übergeben der Länge 0 (null). Beispiel: Konstante 0 (null) als Länge an die **memset-Funktion.**
-   C4319: Not-Operator. Beispiel: "~": Null, die "unsigned long" auf "unsigned \_ int64" mit größerer Größe erweitert.
-   C4313: Aufrufen der **printf-Funktionsfamilie** mit konfliktverursachenden Konvertierungstypspezifizierern und Argumenten. Beispiel: "printf": "%p" in der Formatzeichenfolge weist einen Konflikt mit Argument 2 vom Typ \_ "int64" auf. Ein weiteres Beispiel ist der Aufruf printf("%x", \_ Zeigerwert). Dies führt zu einer Kürzung der oberen 32 Bits. Der richtige Aufruf ist printf("%p", \_ Zeigerwert).
-   C4244: Entspricht der vorhandenen Warnung C4242. Beispiel: "return": Konvertierung von \_ "int64" in "unsigned int", möglicher Datenverlust.

## <a name="64-bit-linker-and-libraries"></a>64-Bit-Linker und Bibliotheken

Verwenden Sie zum Erstellen von Anwendungen den Linker und die Bibliotheken, die vom Windows SDK bereitgestellt werden. Die meisten 32-Bit-Bibliotheken verfügen über eine entsprechende 64-Bit-Version, aber bestimmte Legacybibliotheken sind nur in 32-Bit-Versionen verfügbar. Code, der diese Bibliotheken aufruft, wird nicht verknüpft, wenn die Anwendung für 64-Bit-Windows erstellt wird.

 

 





