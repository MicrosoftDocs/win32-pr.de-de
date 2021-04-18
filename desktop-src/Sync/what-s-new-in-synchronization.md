---
description: Windows umfasst die folgenden neuen Programmier Elemente für die Synchronisierung.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Neuerungen bei der Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216187"
---
# <a name="whats-new-in-synchronization"></a>Neuerungen bei der Synchronisierung

Windows umfasst die folgenden neuen Programmier Elemente für die Synchronisierung.

## <a name="windows-8"></a>Windows 8

### <a name="new-functions"></a>Neue Funktionen

<dl> <dt>

[**Delta-ynchronizationbarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

Löscht eine Synchronisierungs Barriere.

</dd> <dt>

[**Entersynchronizationbarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Bewirkt, dass der aufrufende Thread auf eine Synchronisierungs Barriere wartet, bis die maximale Anzahl von Threads in die Barriere eingetreten ist.

</dd> <dt>

[**Gejeverlappedresultex**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

Ruft die Ergebnisse eines überlappenden Vorgangs für die angegebene Datei, Named Pipe oder das Kommunikationsgerät innerhalb des angegebenen Timeout Intervalls ab. Der aufrufende Thread kann einen Warn Tabellen-warte Vorgang ausführen.

</dd> <dt>

[**Initializesynchronizationbarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

Gibt die maximale Anzahl von Threads und die Drehungs Anzahl für eine neue Synchronisierungs Barriere an.

</dd> <dt>

[**Waitonaddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

Wartet, bis der Wert an der angegebenen Adresse geändert wird.

</dd> <dt>

[**Wakebyaddressall**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

Aktiviert alle Threads, die darauf warten, dass sich der Wert einer Adresse ändert.

</dd> <dt>

[**Wakebyaddresssingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

Aktiviert einen Thread, der darauf wartet, dass sich der Wert einer Adresse ändert.

</dd> </dl>

### <a name="new-interlocked-functions"></a>Neue Interlocked-Funktionen

<dl> <dt>

[**Interlockedaddnofence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))
</dt> <dd>

Führt eine atomarische Additions Operation für die angegebenen **langen** Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))
</dt> <dd>

Führt eine atomarische Additions Operation für die angegebenen **Longlong** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedandnofence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))
</dt> <dd>

Führt eine atomarische and-Operation für die angegebenen **langen** Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))
</dt> <dd>

Führt eine atomarische and-Operation für die angegebenen **char** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))
</dt> <dd>

Führt eine atomarische and-Operation für die angegebenen **kurzwerte** aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))
</dt> <dd>

Führt eine atomarische and-Operation für die angegebenen **Longlong** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))
</dt> <dd>

Testet das angegebene Bit des angegebenen **LONG64** -Werts und ergänzt dieses. Der Vorgang ist atomarisch.

</dd> <dt>

[**Interlockedbittestandresettings**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))
</dt> <dd>

Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 0 fest. Der Vorgang ist atomarisch und wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.

</dd> <dt>

[**Interlockedbittestandreanlelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))
</dt> <dd>

Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 0 fest. Der Vorgang ist atomarisch und wird mithilfe der Speicherfreigabe Semantik ausgeführt.

</dd> <dt>

[**Interlockedbittestandabtacquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))
</dt> <dd>

Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 1 fest. Der Vorgang ist atomarisch und wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.

</dd> <dt>

[**Interlockedbittestandletrelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))
</dt> <dd>

Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 1 fest. Der Vorgang ist atomarisch und wird mit der Versions Semantik für releasearbeitsspeicher ausgeführt.

</dd> <dt>

[**Interlockedcompareexchangenofence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 32-Bit-Werte und tauscht sich mit einem anderen 32-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus.

</dd> <dt>

[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus. Der Vorgang wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.

</dd> <dt>

[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus. Der Austausch erfolgt mit der Auftrags Semantik für releasearbeitsspeicher.

</dd> <dt>

[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 64-Bit-Werte und tauscht sich mit einem anderen 64-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene 128-Bit-Werte und tauscht sich mit einem anderen 128-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert.

</dd> <dt>

[**Interlockedcompareexchangepointernofence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))
</dt> <dd>

Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus. Die-Funktion vergleicht zwei angegebene Zeiger Werte und tauscht mit einem anderen Zeiger Wert auf der Grundlage des Ergebnisses des Vergleichs aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockeddecrementnofence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))
</dt> <dd>

Verringert den Wert der angegebenen 32-Bit-Variablen als atomarischen Vorgang (verringert um 1). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1).

</dd> <dt>

[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))
</dt> <dd>

Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1). Der Vorgang wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.

</dd> <dt>

[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))
</dt> <dd>

Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1). Der Vorgang wird mit der Versions Semantik für releasearbeitsspeicher ausgeführt.

</dd> <dt>

[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))
</dt> <dd>

Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))
</dt> <dd>

Verringert den Wert der angegebenen 64-Bit-Variablen als atomarischen Vorgang (verringert um 1). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedexchangenofence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))
</dt> <dd>

Legt eine 64-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

Legt eine 8-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.

</dd> <dt>

[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))
</dt> <dd>

Legt eine 16-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest. Der Vorgang wird mithilfe der Semantik zum Abrufen der Speicher Reihenfolge ausgeführt.

</dd> <dt>

[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))
</dt> <dd>

Legt eine 16-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))
</dt> <dd>

Legt eine 64-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedexchangepointernofence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))
</dt> <dd>

Tauscht atomisch ein Adress Paar aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedexchangeaddnofence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))
</dt> <dd>

Führt eine atomarische Addition von 2 32-Bit-Werten aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))
</dt> <dd>

Führt eine atomarische Addition von 2 64-Bit-Werten aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedinkrementnofence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))
</dt> <dd>

Erhöht den Wert der angegebenen 32-Bit-Variablen als atomarischen Vorgang (um 1 erhöht). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).

</dd> <dt>

[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))
</dt> <dd>

Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht). Der Vorgang wird mithilfe der Semantik zum Abrufen der Speicher Reihenfolge ausgeführt.

</dd> <dt>

[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))
</dt> <dd>

Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht). Der Vorgang wird mithilfe der Semantik der releasespeicherreihenfolge ausgeführt.

</dd> <dt>

[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))
</dt> <dd>

Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))
</dt> <dd>

Erhöht den Wert der angegebenen 64-Bit-Variablen als atomarischen Vorgang (um 1 erhöht). Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedornofence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))
</dt> <dd>

Führt eine atomarische OR-Operation für die angegebenen **langen** Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))
</dt> <dd>

Führt eine atomarische OR-Operation für die angegebenen **char** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))
</dt> <dd>

Führt eine atomarische OR-Operation für die angegebenen **kurzwerte** aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))
</dt> <dd>

Führt eine atomarische OR-Operation für die angegebenen **Longlong** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**Interlockedpushlistslistex**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein. Der Zugriff auf die Listen wird auf einem Multiprozessorsystem synchronisiert. Diese Version der-Methode verwendet nicht die [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) -Aufruf Konvention.

</dd> <dt>

[**Interlockedxornofence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))
</dt> <dd>

Führt eine atomarische XOR-Operation für die angegebenen **langen** Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))
</dt> <dd>

Führt eine atomarische XOR-Operation für die angegebenen **char** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))
</dt> <dd>

Führt eine atomarische XOR-Operation für die angegebenen **kurzwerte** aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> <dt>

[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))
</dt> <dd>

Führt eine atomarische XOR-Operation für die angegebenen **Longlong** -Werte aus. Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.

</dd> </dl>

## <a name="windows-7"></a>Windows 7

### <a name="new-functions"></a>Neue Funktionen

<dl> <dt>

[**Setwaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

Aktiviert den angegebenen ausnutzbaren Timer und stellt Kontextinformationen für den Timer bereit.

</dd> <dt>

[**Tryacquiresrwlockexclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

Versucht, eine SRW-Sperre (Slim Reader/Writer) im exklusiven Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.

</dd> <dt>

[**Tryacquiresrwlockshared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

Versucht, eine SRW-Sperre (Slim Reader/Writer) im freigegebenen Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.

</dd> </dl>

### <a name="new-structures"></a>Neue Strukturen

<dl> <dt>

[**Grund \_ Kontext**](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

Enthält Kontextinformationen für einen mit [**setwaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)aktivierten Timer.

</dd> </dl>

 

 
