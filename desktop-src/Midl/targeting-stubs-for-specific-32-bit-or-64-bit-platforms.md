---
title: Zielstubs für bestimmte 32-Bit- oder 64-Bit-Plattformen
description: Einige der Features von Microsoft RPC und den MIDL 3.0- und höher-Compilern sind plattformspezifisch.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL für 32-Bit-Plattformen
- 64-Bit-Plattformen MIDL
- Stubs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641170"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Zielstubs für bestimmte 32-Bit- oder 64-Bit-Plattformen

Einige der Features von Microsoft RPC und den MIDL 3.0- und höher-Compilern sind plattformspezifisch.

Als Vorsichtsmaßnahme generieren die MIDL 3.0- und höher-Compiler Schutzmaßnahmen, die die Kompatibilitätsüberprüfung während der C-Kompilierungsphase erleichtern. MIDL generiert zwei Arten von Wächtern: einen plattformabhängigen Wächter (32-Bit im Vergleich zu 64-Bit) und einen releaseabhängigen Schutz (Featuresatzabhängigkeit). MIDL generiert beispielsweise den folgenden Schutz, um die C-Kompilierung eines 32-Bit-Stubs für andere Plattformen zu verhindern:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

Der releaseabhängige Schutz wird durch eine Reihe von Features in den verarbeiteten IDL-Dateien und durch den [**Schalter /target**](-target.md) ausgelöst. Wenn die Schnittstelle beispielsweise Features verwendet, die nur unter Windows 2000 oder höher unterstützt werden, generiert MIDL einen Wächter mit dem Makro TARGET \_ IS \_ NT50 \_ ODER \_ LATER.

Die in Rpcndr.h definierten Schutzmakros hängen von der Einstellung von WINVER und WIN32 WINNT ab und werden vom \_ \_ C/C++-Compiler ausgewertet.

Wenn Sie zur C-Kompilierungszeit eine Fehlermeldung erhalten, die angibt, dass Sie eine bestimmte Plattform zum Ausführen eines Stubs benötigen, überprüfen Sie zunächst, ob Sie ein Feature verwendet haben, das auf dieser Plattform nicht verfügbar ist. Die Features, die einen bestimmten Wächter auslösen, werden im Text des Wächters aufgeführt. Im vorherigen Beispiel hat der Compilerschalter -Oicf den Schutz ausgelöst. Zu den wichtigsten Features dieser Art gehören der Schalter [**/robust**](-robust.md) und das asynchrone Attribut, das unter \[ [](async.md) \] Windows 2000 [](pipe.md) und höher verfügbar ist, der Pipetypkonstruktor, die Compileroption /Oif und die Marshall- und \[ [**\_**](user-marshal.md) \] \[ [**Wire \_ Marshal-Attribute**](wire-marshal.md) des \] Benutzers. Stubs, die diese Features verwenden, werden auf früheren Systemen nicht ausgeführt.

Wenn Sie wissen, dass Ihre Zielplattform für die von Ihnen verwendeten Features korrekt ist und trotzdem ein Fehler auftritt, müssen Sie die Umgebungsvariablen möglicherweise entsprechend festlegen.

**So erstellen Sie für Windows 2000 oder höher**

-   Fügen Sie Ihrem Makefile diese Zeile hinzu:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**Asynchrone**](async.md)
</dt> <dt>

[**Async \_ uuid**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Rohr**](pipe.md)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> <dt>

[**\_Benutzer-Marshalling**](user-marshal.md)
</dt> <dt>

[Marshallen von OLE-Datentypen](marshaling-ole-data-types.md)
</dt> </dl>

 

 




