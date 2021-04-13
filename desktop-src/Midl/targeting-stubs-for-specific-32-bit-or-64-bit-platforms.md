---
title: Stubziele für bestimmte 32-Bit-oder 64-Bit-Plattformen
description: Einige Features von Microsoft RPC und die Compl 3,0 und spätere Compiler sind plattformspezifisch.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- 32-Bit-Plattformen (Mitte)
- 64-Bit-Plattformen (Mitte)
- Stubel-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310731"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Stubziele für bestimmte 32-Bit-oder 64-Bit-Plattformen

Einige Features von Microsoft RPC und die Compl 3,0 und spätere Compiler sind plattformspezifisch.

Als Vorsichtsmaßnahme generieren die Compl 3,0-und spätere Compiler Wächter, die während der C-Kompilierungs Phase die Kompatibilitäts Überprüfung vereinfachen. In der Mitte werden zwei Arten von Wächter generiert: ein Platt Form abhängiger Wächter (32-Bit und 64-Bit) und ein Freigabe abhängiger Wächter (Funktionsgruppen Abhängigkeit). Beispielsweise generiert "Mittel l" den folgenden Schutz, um die C-Kompilierung eines 32-Bit-Stubs für andere Plattformen zu verhindern:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

Der Release-abhängige Wächter wird durch eine Reihe von Funktionen ausgelöst, die in den verarbeiteten IDL-Dateien und durch den [**/target**](-target.md) -Schalter gefunden werden. Wenn die Schnittstelle z. b. Funktionen verwendet, die nur unter Windows-2000 oder höher unterstützt werden, generiert die-Schnittstelle einen Wächter mit dem Target- \_ \_ \_ Makro NT50 oder höher \_ .

Die in Rpcndr. h definierten Wächter Makros hängen von der Einstellung von WINVER und \_ Win32 \_ Winnt ab und werden vom C/C++-Compiler ausgewertet.

Wenn Sie zum Zeitpunkt der C-Kompilierung eine Fehlermeldung erhalten, die besagt, dass Sie eine bestimmte Plattform zum Ausführen eines Stubs benötigen, stellen Sie zunächst sicher, dass Sie kein Feature verwendet haben, das auf dieser Plattform nicht verfügbar ist. Die Funktionen, die einen bestimmten Wächter auslösen, werden im Hauptteil des Schutzes aufgelistet. Im vorherigen Beispiel hat der-Oicf-Compilerschalter den Wächter ausgelöst. Zu den wesentlichen Features dieser Art gehören der [**/robust**](-robust.md) -Switch und das \[ [**Async**](async.md) -Attribut, das \] unter Windows 2000 und höher verfügbar [](pipe.md) ist, der pipetypkonstruktor, die/OIF-Compileroption und die \[ Attribute [**User \_ Marshal**](user-marshal.md) \] und \[ [**Wire \_ Marshal**](wire-marshal.md) \] . Stusb, die diese Features verwenden, werden nicht auf früheren Systemen ausgeführt.

Wenn Sie wissen, dass Ihre Zielplattform für die Features richtig ist, die Sie verwenden und weiterhin einen Fehler erhalten, müssen Sie möglicherweise die Umgebungsvariablen entsprechend festlegen.

**So erstellen Sie für Windows-Versionen 2000 oder höher**

-   Fügen Sie die folgende Zeile zu Makefile hinzu:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**/Target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**Async- \_ UUID**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Kanal**](pipe.md)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> <dt>

[**Benutzer \_ Mars Hall**](user-marshal.md)
</dt> <dt>

[Marshalling von OLE-Datentypen](marshaling-ole-data-types.md)
</dt> </dl>

 

 




