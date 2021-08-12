---
title: Weitere Überlegungen
description: Beachten Sie beim Portieren Ihres Codes die folgenden Punkte.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Tipps zum Portieren von 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 199f522bebf0d6d5552aa81d99aab12f77685dea35eb329b9e7d11d46b4f1500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561535"
---
# <a name="additional-considerations"></a>Weitere Überlegungen

Beachten Sie beim Portieren Ihres Codes die folgenden Punkte:

- Die folgende Annahme ist nicht mehr gültig:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Der 64-Bit-Compiler definiert jedoch \_ WIN32 aus Gründen der Abwärtskompatibilität.

- Die folgende Annahme ist nicht mehr gültig:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   In diesem Fall kann die else-Klausel \_ WIN32 oder \_ WIN64 darstellen.

- Seien Sie vorsichtig bei der Ausrichtung des Datentyps. Das **TYPE \_ ALIGNMENT-Makro** gibt die Ausrichtungsanforderungen eines Datentyps zurück. Beispiel: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 auf x86, 8 auf Intel Itanium-Prozessor `TYPE_ALIGNMENT( UCHAR )` == 1 überall

    Ein Beispiel hierfür ist Kernelcode, der derzeit wie folgt aussieht:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    sollte wahrscheinlich in geändert werden:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Automatische Korrekturen von Kernelmodusausnahmen werden für Intel Itanium-Systeme deaktiviert.

- Seien Sie bei NOT-Vorgängen vorsichtig. Beachten Sie Folgendes:

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    Das Problem besteht darin, dass ~(b–1) "0x0000 0000 xxxx xxxx" und nicht "0xFFFF FFFF xxxx xxxx" erzeugt. Der Compiler erkennt dies nicht. Ändern Sie den Code wie folgt, um dies zu beheben:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Seien Sie vorsichtig, wenn Sie Vorgänge ohne Vorzeichen und mit Vorzeichen ausführen. Beachten Sie Folgendes:

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    Das Ergebnis ist unerwartet groß. Die Regel ist, dass das Ergebnis unsigned ist, wenn einer der Operanden nicht signiert ist. Im vorherigen Beispiel wird ein in einen Wert ohne Vorzeichen konvertiert, dividiert durch b, und das In c gespeicherte Ergebnis. Die Konvertierung umfasst keine numerische Bearbeitung.

    Betrachten Sie als weiteres Beispiel Folgendes:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    Das Problem tritt auf, weil x nicht signiert ist, wodurch der gesamte Ausdruck nicht signiert ist. Dies funktioniert einwandfrei, es sei denn, y ist negativ. In diesem Fall wird y in einen Wert ohne Vorzeichen konvertiert. Der Ausdruck wird mit 32-Bit-Genauigkeit ausgewertet, skaliert und pVar1 hinzugefügt. Eine negative 32-Bit-Zahl ohne Vorzeichen wird zu einer großen positiven 64-Bit-Zahl, die das falsche Ergebnis liefert. Um dieses Problem zu beheben, deklarieren Sie x als signierten Wert, oder geben Sie ihn im Ausdruck explizit in **LONG** ein.

- Seien Sie vorsichtig, wenn Sie stückweise Größenzuordnungen vornehmen. Beispiel:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    Der folgende Code ist falsch, da der Compiler die -Struktur mit weiteren 4 Bytes aufgefüllt, um die 8-Byte-Ausrichtung zu erzielen:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    Der folgende Code ist richtig:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Übergeben Sie nicht `(HANDLE)0xFFFFFFFF` an Funktionen wie [**CreateFileMapping.**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) Verwenden Sie stattdessen **INVALID \_ HANDLE \_ VALUE**.
- Verwenden Sie beim Drucken einer Zeichenfolge die richtigen Formatbezeichner. Verwenden Sie %p, um Zeiger in Hexadezimal zu drucken. Dies ist die beste Wahl für das Drucken von Zeigern. Microsoft Visual C++ unterstützt %I zum Drucken polymorpher Daten. Visual C++ unterstützt auch %I64 zum Drucken von Werten mit 64 Bits.

 

 