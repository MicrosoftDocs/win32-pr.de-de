---
title: Die Tools
description: In diesem Thema werden die Tools beschrieben, die Sie bei der Verwendung von bereitstellen können, um Ihre 64 Anwendung zu erstellen. Windows 10 ist für x64-und ARM64-basierte Prozessoren verfügbar.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Tools
- Tools 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388599"
---
# <a name="the-tools"></a>Die Tools

In diesem Thema werden die Tools beschrieben, die Sie bei der Verwendung von bereitstellen können, um Ihre 64 Anwendung zu erstellen. Windows 10 ist für x64-und ARM64-basierte Prozessoren verfügbar.

## <a name="include-files"></a>Includedateien

Die API-Elemente sind zwischen 32-und 64-Bit-Fenstern praktisch identisch. Die Windows-Header Dateien wurden so geändert, dass Sie sowohl für 32-als auch für 64-Bit-Code verwendet werden können. Die neuen 64-Bit-Typen und-Makros werden in der neuen Header Datei "basetsd. h" definiert, die sich im Satz der in Windows. h enthaltenen Header Dateien befindet. Basetsd. h enthält die neuen Datentyp Definitionen zur Unterstützung bei der Kenn Wort Größe des Quellcodes.

## <a name="new-data-types"></a>Neue Datentypen

Die Windows-Header Dateien enthalten neue Datentypen. Diese Typen sind in erster Linie für die Typkompatibilität mit den 32-Bit-Datentypen vorgesehen. Die neuen Typen bieten genau dieselbe Typisierung wie die vorhandenen Typen, während gleichzeitig die Unterstützung für die 64-Bit-Windows-Bereitstellung unterstützt wird. Weitere Informationen finden Sie in [den neuen Datentypen](the-new-data-types.md) oder in der Header Datei "basetsd. h".

## <a name="predefined-macros"></a>Vordefinierte Makros

Der Compiler definiert die folgenden Makros, um die Plattform zu identifizieren.



| Makro   | Bedeutung                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_Win64 | Eine 64-Bit-Plattform. Dies schließt sowohl x64 als auch ARM64 ein.                                                        |
| \_Win32 | Eine 32-Bit-Plattform. Dieser Wert wird auch vom 64-Bit-Compiler aus Gründen der Abwärtskompatibilität definiert.<br/> |
| \_Win16 | Eine 16-Bit-Plattform                                                                                           |



 

Die folgenden Makros sind spezifisch für die-Architektur.



| Makro      | Bedeutung                |
|------------|------------------------|
| \_M \_ ia64  | Intel Itanium-Plattform |
| \_M \_ IX86  | x86-Plattform           |
| \_M \_ x64   | x64-Plattform           |
| \_M \_ ARM64 | ARM64-Plattform         |



 

Verwenden Sie diese Makros nicht nur mit Architektur spezifischem Code, sondern verwenden Sie stattdessen \_ Win64, \_ Win32 und \_ Win16, wenn dies möglich ist.

## <a name="helper-functions"></a>Hilfsfunktionen

Die folgenden Inline Funktionen (in basetsd. h definiert) können Ihnen helfen, Werte problemlos von einem Typ in einen anderen zu konvertieren.

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
> **Inttoptr** signiert den **int** -Wert, **uinttoptr** NULL erweitert den ganzzahligen **int** -Wert, **longtoptr** signiert den **Long** -Wert, und **ulongtoptr** NULL erweitert den Long-Wert **ohne** Vorzeichen.

 

## <a name="64-bit-compiler"></a>64-Bit-Compiler

Die 64-Bit-Compiler können verwendet werden, um Zeiger abkürzen, falsche Typumwandlungen und andere 64-Bit-spezifische Probleme zu identifizieren.

Wenn der Compiler zum ersten Mal ausgeführt wird, generiert er wahrscheinlich viele Zeiger abkürzen oder Typen Konflikt Warnungen, wie z. b. die folgenden:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Verwenden Sie diese Warnungen als Leitfaden, um den Code stabiler zu machen. Es empfiehlt sich, alle Warnungen zu eliminieren, insbesondere Warnungen für Zeiger abkürzen.

## <a name="64-bit-compiler-switches-and-warnings"></a>64-Bit-Compilerschalter und-Warnungen

Beachten Sie, dass dieser Compiler das LLP64-Datenmodell aktiviert.

Es gibt eine Warn Option, die das Portieren von LLP64 unterstützt. Der Schalter-Wp64-w3 aktiviert die folgenden Warnungen:

-   C4305: trunationwarnung. Beispiel: "Return": Abschneiden von "unsigned Int64" in "Long".
-   C4311: trunationwarnung. Beispiel: "Typumwandlung": Zeiger Verkürzung von "int \* \_ ptr64" in "int".
-   C4312: Konvertierung in eine größere warnungsgrößenwarnung. Beispiel: "Typumwandlung": Konvertierung von "int" in "int \* \_ ptr64" von größerer Größe.
-   C4318: Länge 0 (null). Übergeben Sie z. b. Konstante NULL als Länge an die **memset** -Funktion.
-   C4319: Not-Operator. Beispiel: "~": keine Erweiterung von "unsigned long" in "unsigned \_ Int64" von größerer Größe.
-   C4313: Aufrufen der **printf** -Funktions Familie mit in Konflikt stehenden konvertierungstypspezifizierer und-Argumenten. Beispielsweise steht "printf": "% p" in der Format Zeichenfolge in Konflikt mit Argument 2 vom Typ " \_ Int64". Ein weiteres Beispiel ist der callf-Ausdruck ("% x", Zeiger \_ Wert). Dies bewirkt, dass die oberen 32 Bits abgeschnitten werden. Der richtige-Rückruf ist printf ("% p", Zeiger \_ Wert).
-   C4244: identisch mit der vorhandenen Warnung C4242. Beispiel: "Return": Konvertierung von " \_ Int64" in "unsigned int", möglicher Datenverlust.

## <a name="64-bit-linker-and-libraries"></a>64-Bit-Linker und-Bibliotheken

Verwenden Sie zum Erstellen von Anwendungen den Linker und die Bibliotheken, die von der Windows SDK bereitgestellt werden. Die meisten 32-Bit-Bibliotheken verfügen über eine entsprechende 64-Bit-Version, aber bestimmte Legacy Bibliotheken sind nur in 32-Bit-Versionen verfügbar. Code, der diese Bibliotheken aufruft, kann nicht verknüpft werden, wenn die Anwendung für 64-Bit-Windows erstellt wird.

 

 





