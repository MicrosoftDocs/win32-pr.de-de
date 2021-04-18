---
description: Die Namen und Beschreibungen aller Leistungs Objekte und deren Indikatoren werden in der Registrierung gespeichert.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359047"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung

> [!IMPORTANT]
> Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar. Stattdessen empfiehlt Microsoft die Verwendung der unter [Bereitstellen von Indikator Daten mit Version 2,0](providing-counter-data-using-version-2-0.md) beschriebenen Methode zum Erstellen neuer Leistungsindikatoren und die Migration vorhandener Leistungsindikatoren zur Verwendung dieser Methode.

Die Namen und Beschreibungen aller v1-Leistungs Objekte und deren Zähler müssen auf dem System installiert sein. So speichern Sie Namen und Beschreibungen für die Objekte und Leistungsindikatoren Ihres [v1-Anbieters](providing-counter-data.md):

- [Erstellen Sie eine h-Header Datei](#creating-a-symbolic-constants-h-file) , die die symbolischen Konstanten für die Offsets für die Objekte und Leistungsindikatoren enthält.
- [Erstellen Sie eine Initialisierung (. INI-Datei](#creating-an-initialization-ini-file) , die die Zeichen folgen enthält.
- Wenn Sie die Komponente installieren, [führen Sie das **Lodctr** -Tool](#running-the-lodctr-tool) aus, um die Namen und Beschreibungen in der Registrierung zu installieren.
- Wenn Sie die Komponente deinstallieren, führen Sie das unlodctr-Tool aus, um die Namen und Beschreibungen aus der Registrierung zu entfernen.

## <a name="creating-a-symbolic-constants-h-file"></a>Erstellen einer symbolischen Konstanten Datei (. h)

Erstellen Sie eine h-Header Datei, die Konstanten (Makros) für die Offsets für die Objekte und Leistungsindikatoren definiert, die Ihr Anbieter bereitstellt. Der. h-Header wird während der Installation des Anbieters als Eingabe für **Lodctr** verwendet und kann auch vom C/C++-Code des Anbieters verwendet werden.

Die Konstanten Werte müssen aufeinander folgen, auch Zahlen, die mit 0 (null) beginnen. Gruppieren Sie die Konstanten nach Objekten (d. h. Starten Sie jede Gruppe mit dem Objekt Offset, und folgen Sie dann den Offsets der Zähler für dieses Objekt).

Die Konstanten in der Kopfzeile bestimmen die Reihenfolge, in der die Indikatoren dem Namen und dem Hilfetext in der Registrierung hinzugefügt werden. Der Anbieter verwendet die Offsets, um zu bestimmen, welches Objekt abgefragt wird und welche Indexwerte verwendet werden sollen, wenn die Daten zurückgegeben werden. Weitere Informationen finden Sie unter [Implementieren von openperformancedata](implementing-openperformancedata.md).

Im folgenden finden Sie ein Beispiel für eine symbolische Konstante Datei mit dem Namen counteroffsets. h, die im Beispiel zum [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md) verwendet wird.

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

## <a name="creating-an-initialization-ini-file"></a>Erstellen einer Initialisierung (. INI-Datei

Die Initialisierung (. INI) enthält den Namen und die Hilfe Zeichenfolgen für die einzelnen Objekte und Leistungsdaten, die in der Symbol Datei definiert sind. Die. Die INI-Datei wird während der Installation des Anbieters als Eingabe für **Lodctr** verwendet.

Die. Die INI-Datei muss als UTF-16LE (mit Byte Reihenfolge Markierung) codiert werden und sollte die folgenden Abschnitte und Schlüssel aufweisen:

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

### <a name="info-section"></a>Abschnitt [Info]

Der `[info]` Abschnitt enthält allgemeine Informationen zum Anbieter. Die Abschnitts Schlüssel werden wie folgt definiert:

|Schlüssel|BESCHREIBUNG
|---|-----------
|**DriverName**| Geben Sie den Namen des Leistungs Schlüssels des Anbieters an, der sich in der Registrierung unter dem `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` Schlüssel befindet. Weitere Informationen zum Erstellen dieses Schlüssels finden Sie unter [Erstellen des Leistungs Schlüssels der Anwendung](creating-the-applications-performance-key.md).
|**Symbol file**| Geben Sie die. h-Header Datei an, die symbolische Werte der Objekte und Leistungsindikatoren Ihres Anbieters enthält. Während der Installation (beim Aufrufen von **Lodctr**) muss sich die Header Datei im selben Verzeichnis wie das befinden. INI-Datei.
|**Würdiges**| Wenn Sie diesen Schlüssel in den `[info]` Abschnitt einschließen, fügt **Lodctr** dem Leistungs Schlüssel einen Bibliotheks Überprüfungs Code-Registrierungs Wert mit einer binären Signatur ihrer Leistungs-dll hinzu. Wenn Perflib Ihre DLL aufruft, vergleicht Sie die Signatur mit der dll, um zu bestimmen, ob die DLL geändert wurde. Der Wert des **vertrauenswürdigen** Schlüssels wird ignoriert.

Die `DriverName` `SymbolFile` Schlüssel und sind erforderlich.

### <a name="objects-section"></a>Abschnitt [Objekte]

Der `[objects]` Abschnitt enthält eine Liste der Leistungs Objekte, die vom Anbieter unterstützt werden. Dies wird verwendet, um zu bestimmen, ob jedes Symbol aus dem `[text]` Abschnitt auf ein Objekt oder einen Zählers verweist.

Fügen Sie für jedes Objekt (Counter Set), das vom Anbieter unterstützt wird, dem Abschnitt einen Schlüssel mit dem Namen hinzu `<symbol>_<langid>_NAME=` `[objects]` , wobei `<symbol>` der Name des Objekts und `<langid>` die Sprach-ID einer der unterstützten Sprachen ist. Der Wert wird ignoriert.

> [!IMPORTANT]
> Der `[objects]` Abschnitt verbessert die Leistung des Systems. Obwohl der Abschnitt "Objects" optional ist, sollten Sie diesen Abschnitt stets in ihren einschließen. INI-Datei. Wenn Sie diesen Abschnitt einschließen, wird die Leistungs-dll nur aufgerufen, wenn Sie das angeforderte Objekt unterstützen. Wenn Sie den Objekt Abschnitt nicht einschließen, wird die DLL für jede Abfrage aufgerufen, da das System nicht weiß, welche Objekte der Anbieter unterstützt. Wenn der Objekt Abschnitt nicht enthalten ist, generiert **Lodctr** im Anwendungs Ereignisprotokoll eine Meldung, die besagt, dass die. Die INI-Datei enthielt keinen Objekte Abschnitt. Der Ereignis Bezeichner dieser Nachricht ist 2000.

### <a name="languages-section"></a>Abschnitt [Sprachen]

Der `[languages]` Abschnitt enthält eine Liste der sprach Bezeichner jeder Sprache, für die Ihr Anbieter Name und Hilfe Zeichenfolgen bereitstellt. Alle Anbieter sollten `009` (Englisch) unterstützen.

Fügen Sie für jede unterstützte Sprache einen Schlüssel mit dem Namen hinzu `<langid>=` . Der Wert wird ignoriert, aber zu Dokumentationszwecken wird der Wert normalerweise auf den Namen der entsprechenden Sprache festgelegt, z. b. `009=English` .

In den meisten Sprachen sollten Sie den Bezeichner der primären Sprache verwenden. Die komplette Liste der Sprachen-IDs finden Sie in der Header Datei "Winnt. h" unter der Überschrift "primäre Sprach-IDs". Konvertieren Sie den in Winnt. h gefundenen Wert in eine Sequenz von 3 hexadezimalen Ziffern, indem Sie das `0x` Präfix entfernen und führende Ziffern hinzufügen, `0` bis die Sequenz 3 Ziffern lang ist. Um z. b. englische Zeichen folgen (0x9) anzugeben, verwenden Sie 009. Zum Angeben von italienischen Zeichen folgen (0x10) verwenden Sie 010.

Für chinesische und portugiesische Sprachen sind sowohl die primären als auch die unter Sprachen Bezeichner erforderlich. Verwenden Sie 404, 804, 416 oder 816 anstelle von 004 oder 016.

### <a name="text-section"></a>[Text]-Abschnitt

Der `[text]` -Abschnitt enthält den Namen und die Hilfe Zeichenfolgen für die Objekte und Leistungsindikatoren.

Für jedes Objekt oder jeden Gegenstand und für jede unterstützte Sprache müssen Sie einen namens Schlüssel angeben (mit dem Namen oder der Titel Zeichenfolge für das Objekt oder den Counter), und Sie können optional eine Hilfe Taste (mit der Beschreibung oder der Beschreibungs Zeichenfolge für das Objekt oder den Counter) bereitstellen. Die Schlüssel sollten und lauten `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` , wobei `<symbol>` die symbolische Konstante für das Objekt oder den Leistungs Bezeichner (wie in der Datei "symbolische Konstante. h" definiert) und `<langid>` die für diese Zeichenfolge verwendete Sprachen-ID ist.

Beispielsweise werden die englischen Zeichen folgen für einen Counter mit dem Symbol `MY_COUNTER` wie folgt angegeben:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Die Text Schlüssel können in beliebiger Reihenfolge angezeigt werden. Die Text Zeichenfolgen dürfen keine Formatierungszeichen wie Registerkarten enthalten.

### <a name="example-ini-file"></a>INI-Beispieldatei

Im folgenden finden Sie ein Beispiel einer Initialisierungsdatei, die im Beispiel zum [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md) verwendet wird.

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

## <a name="running-the-lodctr-tool"></a>Ausführen des lodctr-Tools

, Um die in Ihrem definierten Namen und Hilfe Zeichenfolgen zu laden. INI-Datei (während der Installation des Anbieters) führen Sie das **Lodctr** -Tool aus dem Ordner aus, der die enthält. INI-Datei und Header Datei. Das Tool ist auf dem Computer enthalten. Sie müssen **Lodctr** mit erhöhten Rechten ausführen. Der-Parameter für **Lodctr** ist der Pfad zu Ihrem. INI-Datei. Beispiel: `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Zum Entladen der Namen und Hilfe Zeichenfolgen (während der Deinstallation) führen Sie das **unlodctr** -Tool aus. Sie müssen **unlodctr** mit erhöhten Rechten ausführen. Der Parameter für **unlodctr** ist der DriverName des Anbieters (der Name des Leistungs Schlüssels des Anbieters). Beispiel: `unlodctr "MyProvider"`.

Vergewissern Sie sich vor dem Ausführen von **Lodctr**, dass Ihre Anwendung über einen Eintrag unter dem **Dienst** Schlüssel verfügt. Weitere Informationen finden Sie unter [Erstellen des Leistungs Schlüssels der Anwendung](creating-the-applications-performance-key.md). Wenn der Schlüssel nicht vorhanden ist, wird die Registrierung von **Lodctr** nicht mit ihren Namen und Beschreibungen aktualisiert.

Als Alternative zum Ausführen von **Lodctr** können Sie [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definiert in "LoadPerf. h") aus dem Installationsprogramm abrufen, um die Beschreibungen der Indikator Namen zu laden. Sie können dann [**unloadperfcountertextstrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) während der Deinstallation von aufgerufen werden.

Das Hilfsprogramm **Lodctr** kopiert die Zeichen folgen aus. INI **-Datei** zu den Indikatoren und **Hilfe** Registrierungs Werten unter den entsprechenden sprach unter Schlüsseln. Wenn der entsprechende sprach Unterschlüssel nicht vorhanden ist, werden die Zeichen folgen für diese Sprache nicht kopiert. Das Hilfsprogramm aktualisiert auch den letzten Wert des **Zählers** und den **letzten Hilfe** Wert. Die Namen und Beschreibungen von Leistungs Zählern werden an folgendem Speicherort in der Registrierung gespeichert.

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

Zusätzlich zum Hinzufügen von Werten unter dem **Perflib** -Schlüssel fügt das **Lodctr** -Tool auch die folgenden Werte zum Knoten **Dienste** für die Anwendung hinzu. In den meisten Fällen haben die Anwendung und der Anbieter eine 1:1-Beziehung. Es ist jedoch möglich, dass ein Anbieter gegen Daten für mehrere Anwendungen bereitstellt. aus diesem Grund basiert der Schlüssel auf der Anwendung und nicht auf dem Anbieter.

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
