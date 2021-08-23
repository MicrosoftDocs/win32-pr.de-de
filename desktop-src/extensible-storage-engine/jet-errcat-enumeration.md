---
description: 'Weitere Informationen finden Sie unter: JET_ERRCAT Enumeration'
title: JET_ERRCAT -Enumeration (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f259edf0e087831cfb667caa5fa8dcf215638ab6d739812fa2e6208327a22f7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232800"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT Enumeration

Die Fehlerkategorie. Die Hierarchie ist wie folgt: JET_errcatError | |- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO / Fehlerhafte E/A-Probleme, kann vorübergehend sein oder nicht. | |- JET_errcatResource | |- JET_errcatMemory / Nicht genügend Arbeitsspeicher (alle Varianten) | |– JET_errcatQuota | |- JET_errcatDisk / Nicht genügend Speicherplatz (alle Varianten) |- |- JET_errcatData | |- JET_errcatCorruption | |- JET_errcatInconsistent " verursacht durch benutzerverfehlte | || |- JET_errcatFragmentation |- JET_errcatApi |- JET_errcatUsage |- JET_errcatState |-- JET_errcatObsolete

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Member

<table>
<thead>
<tr class="header">
<th></th>
<th>Membername</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Unbekannt</td>
<td>Unbekannte Kategorie.</td>
</tr>
<tr class="even">
<td></td>
<td>Fehler</td>
<td>Eine generische Kategorie.</td>
</tr>
<tr class="odd">
<td></td>
<td>Vorgang</td>
<td>Fehler, die in der Regel jederzeit aufgrund nicht kontrollierbarer Bedingungen auftreten können. Häufig temporär, aber nicht immer. Wiederherstellung: Versuchen Sie es wahrscheinlich erneut, oder informieren Sie den Operator schließlich.</td>
</tr>
<tr class="even">
<td></td>
<td>Schwerwiegend</td>
<td>Dieser Sortierfehler tritt nur auf, wenn ESE auf eine Fehlerbedingung trifft, die so unerschädlich ist, dass wir nicht auf sichere (häufig transaktionale) Weise fortfahren können, und anstatt beschädigte Daten zu verursachen, werden Fehler dieser Kategorie ausgegeben. Wiederherstellung: Starten Sie die Instanz oder den Prozess neu. Wenn das Problem weiterhin besteht, informieren Sie den Operator.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O-Fehler stammen vom Betriebssystem und liegen nicht unter der Kontrolle der ESE. Diese Art von Fehler ist möglicherweise temporär, möglicherweise nicht. Wiederherstellung: Wiederholen Sie den Vorgang. Wenn dies nicht behoben ist, fragen Sie den Operator nach dem Datenträgerproblem.</td>
</tr>
<tr class="even">
<td></td>
<td>Ressource</td>
<td>Dies ist eine Kategorie, die eine von vielen möglichen Nichtressourcenbedingungen angibt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Arbeitsspeicher</td>
<td>Klassische Bedingung für nicht genügend Arbeitsspeicher. Wiederherstellung: Warten Sie eine Weile, und wiederholen Sie den Vorgang, geben Sie Arbeitsspeicher frei, oder beenden Sie den Vorgang.</td>
</tr>
<tr class="even">
<td></td>
<td>Kontingent</td>
<td>Bestimmte spezielle Ressourcen befinden sich in Pools einer bestimmten Größe, wodurch es einfacher &quot; &quot; ist, Lecks dieser Ressourcen zu erkennen. Wiederherstellung: Möglicherweise sind einige geringfügige Codeänderungen erforderlich. Ihre Anwendung sollte unter diesen Bedingungen nur eine Debugaktion (z. B. assert) haben, um sie während der Entwicklung zu erkennen. Für Einzelhandelscode wird empfohlen, diesen Fehler wie den Fehler speicherkategorie zu behandeln und entweder den Vorgang zu wiederholen, Arbeitsspeicher frei zu geben oder den Vorgang zu beenden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Datenträger</td>
<td>Out-of-Disk-Bedingungen. Wiederherstellung: Kann später versuchen, mehr Speicherplatz verfügbar zu machen, oder den Operator bitten, Speicherplatz frei zu geben.</td>
</tr>
<tr class="even">
<td></td>
<td>Daten</td>
<td>Ein datenbezogener Fehler.</td>
</tr>
<tr class="odd">
<td></td>
<td>Korruption</td>
<td>Meine Festplatte hat meine Hausaufgaben gemacht. Klassische Beschädigungsprobleme, häufig dauerhaft ohne Korrekturmaßnahmen. Wiederherstellung: Wiederherstellen aus einer Sicherung, z. B. der Reparaturvorgang der ese-Hilfsprogramme (der nur die datenabgelassenen/verlustgefädigenden Daten entfernt) . Auch im Fall der Wiederherstellung (JetInit) kann die Wiederherstellung möglicherweise durchgeführt werden, indem Datenverluste ermöglicht werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Inkonsistent</td>
<td>Dies ähnelt der Beschädigung, da sich die Datenbank- und/oder Protokolldateien in einem Zustand befinden, der inkonsistent und nicht miteinander in Einklang steht. Dies wird häufig durch eine fehlgeleitete Anwendungs-/Administratorverwaltung verursacht. Wiederherstellung: Wiederherstellen aus einer Sicherung, z. B. der Reparaturvorgang der ese-Hilfsprogramme (der nur die datenabgelassenen/verlustgefädigenden Daten auswies). Auch im Fall der Wiederherstellung (JetInit) kann die Wiederherstellung möglicherweise durchgeführt werden, indem Datenverluste ermöglicht werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentierung</td>
<td>Dies ist eine Fehlerklasse, bei der einige persistente interne Ressourcen nicht mehr verwendet werden. Wiederherstellung: Bei Datenbankfehlern wird das Problem durch die  Offlinedefragmentierung behoben, da die Protokolldateien zunächst alle angefügten Datenbanken nach einem sauberen Herunterfahren wiederherstellen und dann alle Protokolldateien und Prüfpunkte löschen.</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Ein Container für Nutzung und Zustand.</td>
</tr>
<tr class="odd">
<td></td>
<td>Verbrauch</td>
<td>Klassischer Verwendungsfehler: Dies bedeutet, dass der Clientcode keine richtigen Argumente an die JET-API übergeben hat. Dieser Fehler wird wahrscheinlich nicht mit einem Wiederholungsversuch entfernt. Wiederherstellung: Im Allgemeinen sollte client code assert() diese Fehlerklasse nicht zurückgegeben werden, sodass Probleme während der Entwicklung erfasst werden können. Im Einzelhandel hat die App wahrscheinlich nur wenige Optionen, aber das Problem an den Operator zurück zu geben.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Dies ist die Klassifizierung für verschiedene Signale, die die API zurückgeben könnte, um den Status der Datenbank zu beschreiben. Ein klassischer Fall ist JET_errRecordNotFound der von JetSeek() zurückgegeben werden kann, wenn der von Ihnen geforderte Datensatz nicht gefunden wurde. Wiederherstellung: Nicht wirklich relevant, hängt stark von der API ab.</td>
</tr>
<tr class="odd">
<td></td>
<td>Veraltet</td>
<td>Der Fehler wird als gültiger Fehler erkannt, aber es wird nicht erwartet, dass er von dieser Version der API zurückgegeben wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Max</td>
<td>Der Höchstwert für die -Enum. Dies sollte nicht verwendet werden.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
