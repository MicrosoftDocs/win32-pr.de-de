---
title: Weitere Überlegungen
description: Beachten Sie beim Portieren Ihres Codes die folgenden Punkte.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Portieren von Tipps 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106350740"
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

   Der 64-Bit-Compiler definiert \_ Win32 jedoch aus Gründen der Abwärtskompatibilität.

- Die folgende Annahme ist nicht mehr gültig:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   In diesem Fall kann die Else-Klausel \_ Win32 oder \_ Win64 darstellen.

- Achten Sie auf die Ausrichtung des Datentyps. Das **\_ typausrichtungs** Makro gibt die Ausrichtungs Anforderungen eines Datentyps zurück. Beispiel: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 auf x86, 8 auf dem Intel Itanium-Prozessor `TYPE_ALIGNMENT( UCHAR )` = = 1 Everywhere

    Beispiel: Kernel Code, der derzeit wie folgt aussieht:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    sollte wahrscheinlich in geändert werden:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Automatische Korrekturen der kernelmodusausrichtungs-Ausnahmen sind für Intel Itanium-Systeme deaktiviert.

- Seien Sie vorsichtig mit nicht Vorgängen. Beachten Sie Folgendes:

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    Das Problem besteht darin, dass ~ (b – 1) "0x0000 0000 xxxx xxxx" und nicht "0xFFFF FFFF xxxx xxxx" erzeugt. Der Compiler erkennt dies nicht. Um dieses Problem zu beheben, ändern Sie den Code wie folgt:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Achten Sie darauf, nicht signierte und signierte Vorgänge auszuführen. Beachten Sie Folgendes:

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    Das Ergebnis ist unerwartet groß. Die Regel ist, dass das Ergebnis ohne Vorzeichen ist, wenn einer der beiden Operanden nicht signiert ist. Im vorherigen Beispiel wird eine in einen nicht signierten Wert, dividiert durch b, und das in c gespeicherte Ergebnis konvertiert. Die Konvertierung umfasst keine numerische Bearbeitung.

    Beachten Sie als weiteres Beispiel Folgendes:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    Das Problem tritt auf, weil x nicht signiert ist, wodurch der gesamte Ausdruck nicht signiert wird. Dies funktioniert problemlos, es sei denn, y ist negativ. In diesem Fall wird y in einen Wert ohne Vorzeichen konvertiert, der Ausdruck wird mit einer Genauigkeit von 32 Bit ausgewertet, skaliert und zu pVar1 hinzugefügt. Eine negative 32-Bit-Zahl ohne Vorzeichen wird zu einer großen 64-Bit-positiven Zahl, die das falsche Ergebnis liefert. Um dieses Problem zu beheben, deklarieren Sie x als einen signierten Wert, oder legen Sie ihn explizit in **Long** im Ausdruck ab.

- Gehen Sie beim Erstellen von Zuordnungen mit schrittweisen Größen vorsichtig vor. Beispiel:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    Der folgende Code ist falsch, da der Compiler die Struktur mit zusätzlichen 4 Bytes auffüllt, um die 8-Byte-Ausrichtung zu treffen:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    Der folgende Code ist korrekt:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Übergeben Sie nicht `(HANDLE)0xFFFFFFFF` an Funktionen wie z. b. " [**kreatefilemapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)". Verwenden Sie stattdessen **einen ungültigen \_ handle- \_ Wert**.
- Verwenden Sie die richtigen Format Bearbeiter, wenn Sie eine Zeichenfolge drucken. Verwenden Sie% p, um Zeiger in Hexadezimal zu drucken. Dies ist die beste Wahl für das Drucken von Zeigern. Der Microsoft Visual C++ unterstützt% I. zum Drucken von polymorphen Daten. Visual C++ unterstützt auch% I64, um Werte, die 64 Bits sind, zu drucken.

 

 