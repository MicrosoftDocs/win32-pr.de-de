---
description: 'Weitere Informationen finden Sie hier: JET_ERRCAT-Enumeration'
title: JET_ERRCAT-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
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
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216308"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT-Enumeration

Die Fehler Kategorie. Die Hierarchie lautet wie folgt: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//ungültige e/a-Probleme, möglicherweise nicht vorübergehend. | |--JET_errcatResource | |--JET_errcatMemory//nicht genügend Arbeitsspeicher (alle Varianten) | |--JET_errcatQuota | |--JET_errcatDisk//nicht genügend Speicherplatz (alle Varianten) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//in der Regel aufgrund von Benutzer-mishandeln | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Fehler, die in der Regel aufgrund von unkontrollierbaren Bedingungen auftreten können. Häufig temporär, aber nicht immer. Wiederherstellung: Wiederholen Sie den Vorgang, oder Benachrichtigen Sie den Operator schließlich.</td>
</tr>
<tr class="even">
<td></td>
<td>FAT</td>
<td>Dieser Sortier Fehler tritt nur dann auf, wenn ESE auf eine Fehlerbedingung trifft, die nicht in einer sicheren (häufig transaktionalen) Weise fortgesetzt werden kann, und nicht zu beschädigten Daten, da wir Fehler dieser Kategorie auslösen. Wiederherstellung: Starten Sie die Instanz oder den Prozess neu. Wenn das Problem weiterhin besteht, informieren Sie den-Operator.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O-Fehler stammen aus dem Betriebssystem und liegen außerhalb der ESE-Kontrolle. diese Art von Fehler ist möglicherweise temporär, möglicherweise nicht. Wiederherstellung: versuchen Sie es erneut. Wenn das Problem nicht behoben ist, bitten Sie den Operator um Datenträger.</td>
</tr>
<tr class="even">
<td></td>
<td>Resource</td>
<td>Dabei handelt es sich um eine Kategorie, die einen von vielen potenziellen Bedingungen außerhalb der Ressourcen angibt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Arbeitsspeicher</td>
<td>Nicht genügend Arbeitsspeicher. Wiederherstellung: warten Sie einen Moment, und wiederholen Sie den Vorgang, oder beenden Sie den Vorgang.</td>
</tr>
<tr class="even">
<td></td>
<td>Kontingent</td>
<td>Bestimmte &quot; spezialisierte &quot; Ressourcen befinden sich in Pools mit einer bestimmten Größe, sodass Sie Verluste dieser Ressourcen leichter erkennen können. Wiederherstellung: erfordert möglicherweise einige geringfügige Codeänderungen. Die Anwendung sollte über eine Debugaktion (z. b. eine Assert-Aktion) für diese Bedingungen verfügen, um Sie während der Entwicklung zu erkennen. Für den Einzelhandels Code empfiehlt es sich, diesen Fehler wie den Fehler der Arbeitsspeicher Kategorie zu behandeln und entweder einen Wiederholungsversuch auszuführen, Arbeitsspeicher freizugeben oder den Vorgang zu beenden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Datenträger</td>
<td>Nicht genügend Speicherplatz. Wiederherstellung: Wiederholen Sie den Vorgang später in der Hoffnung, dass mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz freizugeben.</td>
</tr>
<tr class="even">
<td></td>
<td>Daten</td>
<td>Ein Daten bezogener Fehler.</td>
</tr>
<tr class="odd">
<td></td>
<td>Bnis</td>
<td>Meine Festplatte meine Hausaufgaben. Klassische Beschädigungs Probleme, häufig permanent ohne Korrekturmaßnahmen. Wiederherstellung: Stellen Sie eine Wiederherstellung von einer Sicherung wieder her, u. u. den ESE-Hilfsprogramme-Reparaturvorgang (der nur die verbleibenden und verlustfreien Daten Im Fall einer Wiederherstellung kann eine Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Einheitlich</td>
<td>Dies ähnelt der Beschädigung, dass sich die Datenbank und/oder die Protokolldateien in einem Zustand befinden, der inkonsistent ist und nicht miteinander zu vereinbaren ist. Dies wird häufig durch eine Anwendungs-/administratormishandelung verursacht. Wiederherstellung: Stellen Sie eine Wiederherstellung von einer Sicherung wieder her, u. u. den ESE-Hilfsprogramme-Reparaturvorgang (der nur die verbleibenden und verlustfreien Daten Im Fall einer Wiederherstellung kann eine Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentierung</td>
<td>Dabei handelt es sich um eine Klasse von Fehlern, bei denen einige persistente interne Ressourcen abgelaufen sind. Wiederherstellung: bei Daten Bank Fehlern wird das Problem durch die Offline Defragmentierung behoben, und für die Protokolldateien werden _zuerst_ alle angefügten Datenbanken in einem fehlerfreien Herunterfahren wieder hergestellt. Anschließend werden alle Protokolldateien und Prüfpunkte gelöscht.</td>
</tr>
<tr class="even">
<td></td>
<td>Found</td>
<td>Ein Container für die Verwendung und den Status.</td>
</tr>
<tr class="odd">
<td></td>
<td>Verbrauch</td>
<td>Klassischer Verwendungs Fehler. Dies bedeutet, dass der Client Code keine korrekten Argumente an die Jet-API übergeben hat. Dieser Fehler wird bei einem Wiederholungsversuch wahrscheinlich nicht fortgesetzt. Wiederherstellung: im Allgemeinen sollte der Client Code Assert () diese Fehler Klasse wird nicht zurückgegeben, sodass Probleme während der Entwicklung abgefangen werden können. Im Einzelhandel hat die APP wahrscheinlich nur wenig Optionen, aber das Problem an den Operator zurückzugeben.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Dies ist die Klassifizierung für verschiedene Signale, die die API zurückgeben könnte, die den Status der Datenbank beschreiben. ein klassischer Fall ist JET_errRecordNotFound, der von JetSeek () zurückgegeben werden kann, wenn der von Ihnen angeforderte Datensatz nicht gefunden wurde. Wiederherstellung: nicht wirklich relevant, hängt stark von der API ab.</td>
</tr>
<tr class="odd">
<td></td>
<td>Veraltet</td>
<td>Der Fehler wird als gültiger Fehler erkannt, es wird jedoch davon ausgegangen, dass er von dieser Version der API nicht zurückgegeben wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Max.</td>
<td>Der Höchstwert für die Enumeration. Dies sollte nicht verwendet werden.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
