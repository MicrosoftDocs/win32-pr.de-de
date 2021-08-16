---
description: Die Namen und Beschreibungen aller Leistungsobjekte und deren Leistungsindikatoren werden in der Registrierung gespeichert.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58333e9694b9aa74ff1d5ade6a399aaa813e7735ea315be529587e813fec0fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794055"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung

> [!IMPORTANT]
> Aufgrund von erheblichen Leistungs- und Zuverlässigkeitseinschränkungen kann die In diesem Thema beschriebene Methode zum Bereitstellen von Leistungsindikatordaten in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft, die in Bereitstellen von Indikatordaten mit Version [2.0](providing-counter-data-using-version-2-0.md) beschriebene Methode zum Erstellen neuer Leistungsindikatoren zu verwenden und vorhandene Leistungsindikatoren zu migrieren, um diese Methode zu verwenden.

Die Namen und Beschreibungen aller V1-Leistungsobjekte und deren Leistungsindikatoren müssen im System installiert werden. So speichern Sie Namen und Beschreibungen für die Objekte und Leistungsindikatoren ihres [V1-Anbieters:](providing-counter-data.md)

- [Erstellen Sie eine H-Headerdatei,](#creating-a-symbolic-constants-h-file) die die symbolischen Konstanten für die Offsets zu Ihren Objekten und Leistungsindikatoren enthält.
- [Erstellen Sie eine Initialisierungsdatei (.INI),](#creating-an-initialization-ini-file) die die Zeichenfolgen enthält.
- Führen Sie beim Installieren der Komponente [das **Tool lodctr** aus,](#running-the-lodctr-tool) um die Namen und Beschreibungen in der Registrierung zu installieren.
- Führen Sie beim Deinstallieren der Komponente das Tool unlodctr aus, um die Namen und Beschreibungen aus der Registrierung zu entfernen.

## <a name="creating-a-symbolic-constants-h-file"></a>Erstellen einer symbolischen Konstantendatei (.h)

Erstellen Sie eine H-Headerdatei, die Konstanten (Makros) für die Offsets zu den Objekten und Leistungsindikatoren definiert, die ihr Anbieter an stellt. Der H-Header wird während der Installation Ihres Anbieters als Eingabe für **lodctr** verwendet und kann auch vom C/C++-Code Ihres Anbieters verwendet werden.

Die konstanten Werte müssen aufeinanderfolgende sein, auch Zahlen, die mit 0 (null) beginnen. Gruppieren Sie die Konstanten nach Objekten (d. h. starten Sie jede Gruppe mit dem Objektoffset, und folgen Sie dann mit den Offsets der Leistungsindikatoren für dieses Objekt).

Die Konstanten im Header bestimmen die Reihenfolge, in der die Leistungsindikatoren dem Namen und Hilfetext in der Registrierung hinzugefügt werden. Der Anbieter verwendet die Offsets, um zu bestimmen, welches Objekt abgefragt wird, und die Indexwerte, die beim Zurückgeben der Daten verwendet werden. Weitere Informationen finden Sie unter [Implementieren von OpenPerformanceData.](implementing-openperformancedata.md)

Das folgende Beispiel zeigt eine symbolische Konstantendatei namens CounterOffsets.h, die im Beispiel [Creating a Performance Extension DLL (Erstellen](creating-a-performance-extension-dll.md) einer Leistungserweiterungs-DLL) verwendet wird.

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Erstellen einer Initialisierungsdatei (.INI)

Die Initialisierungsdatei (.INI) enthält den Namen und die Hilfezeichenfolgen für jedes Objekt und jeden Leistungsindikator, die in der Symboldatei definiert sind. Die .INI wird während der Installation Ihres Anbieters als Eingabe für **lodctr** verwendet.

Die .INI sollte als UTF-16LE (mit Byte-Reihenfolgenmarkung) codiert werden und über die folgenden Abschnitte und Schlüssel verfügen:

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>[Info] Abschnitt

Der `[info]` Abschnitt enthält allgemeine Informationen zum Anbieter. Die Abschnittsschlüssel sind wie folgt definiert:

|Key|Beschreibung
|---|-----------
|**DriverName**| Geben Sie den Namen des Leistungsschlüssels des Anbieters an, der sich in der Registrierung unter dem Schlüssel `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` befindet. Informationen zum Erstellen dieses Schlüssels finden Sie unter [Erstellen des Leistungsschlüssels der Anwendung.](creating-the-applications-performance-key.md)
|**SymbolFile**| Geben Sie die H-Headerdatei an, die symbolische Werte der Objekte und Leistungsindikatoren Ihres Anbieters enthält. Während der Installation (beim Aufrufen von **lodctr)** muss sich die Headerdatei im gleichen Verzeichnis wie die .INI befinden.
|**Vertrauenswürdigen**| Wenn Sie diesen Schlüssel in den Abschnitt eingeben, fügt lodctr ihrem Leistungsschlüssel einen Registrierungswert für den Bibliotheksvalidierungscode mit einer binären Signatur Ihrer `[info]` Leistungs-DLL  hinzu. Wenn PERFLIB Ihre DLL aufruft, wird die Signatur mit Ihrer DLL verglichen, um zu ermitteln, ob die DLL geändert wurde. Der Wert des **vertrauenswürdigen** Schlüssels wird ignoriert.

Die `DriverName` Schlüssel und sind `SymbolFile` erforderlich.

### <a name="objects-section"></a>[Objekte] Abschnitt

Der `[objects]` Abschnitt enthält eine Liste der Leistungsobjekte, die der Anbieter unterstützt. Dies wird verwendet, um zu bestimmen, ob jedes Symbol aus dem Abschnitt `[text]` auf ein Objekt oder einen Zähler verweist.

Fügen Sie für jedes Objekt (Counterset), das von Ihrem Anbieter unterstützt wird, einen Schlüssel namens zum Abschnitt hinzu, wobei der Name des Objekts und die Sprach-ID einer der unterstützten `<symbol>_<langid>_NAME=` `[objects]` Sprachen `<symbol>` `<langid>` ist. Der Wert wird ignoriert.

> [!IMPORTANT]
> Der `[objects]` Abschnitt verbessert die Leistung des Systems. Obwohl der Abschnitt objects optional ist, sollten Sie diesen Abschnitt immer in ihre .INI. Wenn Sie diesen Abschnitt verwenden, wird Ihre Leistungs-DLL nur aufgerufen, wenn Sie das angeforderte Objekt unterstützen. Wenn Sie den Abschnitt objects nicht hinzufügen, wird Ihre DLL für jede Abfrage aufgerufen, da das System nicht weiß, welche Objekte ihr Anbieter unterstützt. Wenn der Objektabschnitt nicht enthalten ist, generiert **lodctr** eine Meldung im Anwendungsereignisprotokoll, die besagt, dass die .INI-Datei keinen Objektabschnitt enthielt. Der Ereignisbezeichner dieser Nachricht ist 2000.

### <a name="languages-section"></a>[Sprachen] Abschnitt

Der Abschnitt enthält eine Liste der Sprachbezeichner der einzelnen Sprachen, für die Ihr Anbieter `[languages]` Namen und Hilfezeichenfolgen an stellt. Alle Anbieter sollten `009` (Englisch) unterstützen.

Fügen Sie für jede unterstützte Sprache einen Schlüssel namens `<langid>=` hinzu. Der Wert wird ignoriert, aber zu Dokumentationszwecken wird der Wert normalerweise auf den Namen der entsprechenden Sprache festgelegt, z. B. `009=English` .

Für die meisten Sprachen sollten Sie den Bezeichner der primären Sprache verwenden. Die vollständige Liste der Sprachbezeichner befindet sich in der Headerdatei Winnt.h unter der Überschrift "Primärsprach-IDs". Konvertieren Sie den in Winnt.h gefundenen Wert in eine Sequenz von drei Hexadezimalziffern, indem Sie das Präfix entfernen und führende Ziffern hinzufügen, bis die Sequenz drei Ziffern `0x` `0` lang ist. Verwenden Sie beispielsweise 009, um englische Zeichenfolgen (0x9 anzugeben. Um italienische Zeichenfolgen (0x10 anzugeben, verwenden Sie 010.

Die Sprachen Chinesisch und Portugiesisch erfordern sowohl den primären als auch den subsprachlichen Bezeichner. Verwenden Sie 404, 804, 416 oder 816 anstelle von 004 oder 016.

### <a name="text-section"></a>[text]-Abschnitt

Der `[text]` Abschnitt enthält den Namen und die Hilfezeichenfolgen für Ihre Objekte und Leistungsindikatoren.

Für jedes Objekt oder jeden Leistungsindikator und für jede unterstützte Sprache müssen Sie einen NAME-Schlüssel angeben (der den Namen oder die Titelzeichenfolge für Ihr Objekt oder Ihren Indikator enthält), und Sie können optional einen HELP-Schlüssel (mit der Beschreibungs- oder Erklärungszeichenfolge für Ihr Objekt oder Ihren Indikator) angeben. Die Schlüssel sollten und benannt werden, wobei die symbolische Konstante für das Objekt oder den Leistungsindikator ist (wie in der symbolischen .h-Datei definiert), und ist der Sprachbezeichner, der für diese `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` `<symbol>` `<langid>` Zeichenfolge verwendet wird.

Die englischen Zeichenfolgen für einen Leistungsindikator mit Symbol `MY_COUNTER` würden beispielsweise wie im folgenden Beispiel angegeben:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Die Texttasten können in beliebiger Reihenfolge angezeigt werden. Die Textzeichenfolgen dürfen keine Formatierungszeichen wie Registerkarten enthalten.

### <a name="example-ini-file"></a>BEISPIEL-INI-Datei

Im Folgenden finden Sie ein Beispiel für eine Initialisierungsdatei, die im Beispiel [Creating a Performance Extension DLL (Erstellen einer Leistungserweiterungs-DLL) verwendet](creating-a-performance-extension-dll.md) wird.

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Ausführen des Lodctr-Tools

Um die Namen und Hilfezeichenfolgen zu laden, die in ihrer .INI-Datei (während der Installation Des Anbieters) definiert sind, führen Sie das **Tool lodctr** aus dem Ordner aus, der ihre .INI-Datei und Headerdatei enthält. Das Tool ist im Computer enthalten. Sie müssen **lodctr mit** erhöhten Rechten ausführen. Der Parameter für **lodctr ist** der Pfad zu Ihrer .INI Datei. Beispiel: `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Führen Sie das **Unlodctr-Tool** aus, um die Namen und Hilfezeichenfolgen (während der Deinstallation) zu entladen. Sie müssen **unlodctr mit** erhöhten Rechten ausführen. Der Parameter für **unlodctr** ist der DriverName Ihres Anbieters (der Name des Leistungsschlüssels des Anbieters). Beispiel: `unlodctr "MyProvider"`.

Stellen Sie **vor dem Ausführen von lodctr** sicher, dass Ihre Anwendung über einen Eintrag unter dem Schlüssel **Dienste** verfügt. Weitere Informationen finden Sie unter [Erstellen des Leistungsschlüssels der Anwendung.](creating-the-applications-performance-key.md) Wenn der Schlüssel nicht vorhanden ist, **aktualisiert lodctr** die Registrierung nicht mit Ihren Namen und Beschreibungen.

Als Alternative zum Ausführen von **lodctr** können Sie [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definiert in Loadperf.h) aus dem Installationsprogramm aufrufen, um die Beschreibungen der Indikatornamen zu laden. Anschließend können Sie [**UnloadPerfCounterTextStrings während der Deinstallation**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) aufrufen.

Das **Hilfsprogramm lodctr** kopiert die Zeichenfolgen aus der .INI datei in die Registrierungswerte **Counters** und **Help** unter den entsprechenden Sprachunterschlüsseln. Wenn der entsprechende Sprachunterschlüssel nicht vorhanden ist, werden die Zeichenfolgen für diese Sprache nicht kopiert. Das Hilfsprogramm aktualisiert auch den **Wert des letzten Leistungsindikators** **und der letzten** Hilfe. Die Namen und Beschreibungen der Leistungsindikatoren werden an folgendem Speicherort in der Registrierung gespeichert.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Zusätzlich zum Hinzufügen von Werten unter dem **PerfLib-Schlüssel** fügt das  **Tool lodctr** dem Knoten Dienste für die Anwendung auch die folgenden Werte hinzu. In den meisten Fällen verfügen die Anwendung und der Anbieter über eine 1:1-Beziehung. Es ist jedoch möglich, dass ein Anbieter Leistungsindikatordaten für mehrere Anwendungen zur Verfügung stellt. Aus diesem Grund basiert der Schlüssel auf der Anwendung und nicht auf dem Anbieter.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
