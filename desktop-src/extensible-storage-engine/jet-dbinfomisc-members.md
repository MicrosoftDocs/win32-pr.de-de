---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC Member'
title: 'JET_DBINFOMISC-Member '
TOCTitle: JET_DBINFOMISC members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc_members(v=EXCHG.10)
ms:contentKeyID: 39515834
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c43b9b158bc0b3b9c0f1e56752b3121b467bf1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861960"
---
# <a name="jet_dbinfomisc-members"></a>JET_DBINFOMISC-Member 

Geschützte Member einschließen  
Geerbte Member einschließen  

Enthält verschiedene Informationen zu einer Datenbank. Dies sind die Informationen, die im Daten Bank Header enthalten sind.

Der [JET_DBINFOMISC](./jet-dbinfomisc-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="constructors"></a>Konstruktoren

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh566519(v=exchg.10).md">JET_DBINFOMISC</a></td>
<td></td>
</tr>
</tbody>
</table>


Oben

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578821(v=exchg.10).md">bkinfocopyprev</a></td>
<td>Ruft Informationen zur letzten erfolgreichen Kopiesicherung ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565264(v=exchg.10).md">bkinfodiffprev</a></td>
<td>Ruft Informationen zur letzten erfolgreichen differenziellen Sicherung ab. Wird zurückgesetzt, wenn <a href="hh577635(v=exchg.10).md">bkinfofullprev</a> festgelegt ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577657(v=exchg.10).md">bkinfofullcur</a></td>
<td>Ruft Informationen zur aktuellen Sicherung ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577635(v=exchg.10).md">bkinfofullprev</a></td>
<td>Ruft Informationen zur letzten erfolgreichen vollständigen Sicherung ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh564433(v=exchg.10).md">bkinfoincprev</a></td>
<td>Ruft Informationen über die letzte erfolgreiche inkrementelle Sicherung ab. Dieser Wert wird zurückgesetzt, wenn <a href="hh577635(v=exchg.10).md">bkinfofullprev</a> festgelegt ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578850(v=exchg.10).md">cbpagesize</a></td>
<td>Ruft die Größe der Datenbankseite ab. Der Wert 0 bedeutet 4-KB-Seiten.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh558061(v=exchg.10).md">dbstate</a></td>
<td>Ruft den konsistenten/inkonsistenten Status der Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></td>
<td>Ruft die Buildnummer des Betriebssystems aus dem letzten anfügen ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></td>
<td>Ruft die Hauptversion des Betriebssystems ab dem letzten anfügen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></td>
<td>Ruft die neben Version des Betriebssystems aus dem letzten anfügen ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh564660(v=exchg.10).md">' f ' wingdeaktiviert</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Katalog schattung aktiviert ist. Dieser Wert ist nur für die interne Verwendung vorgesehen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565757(v=exchg.10).md">FUpgrade DB</a></td>
<td>Ruft einen Wert ab, der angibt, ob die Datenbank aktualisiert wird. Dieser Wert ist nur für die interne Verwendung vorgesehen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh579055(v=exchg.10).md">gencommit</a></td>
<td>Ruft die maximale Protokoll Generierung ab, die für die Datenbank ausgeführt wurde. In der Regel die aktuelle Protokoll Generierung.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh579109(v=exchg.10).md">genmaxrequired</a></td>
<td>Ruft die maximale Protokoll Generierung ab, die für die Wiedergabe der Protokolle erforderlich ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565891(v=exchg.10).md">genminrequired</a></td>
<td>Ruft die minimale Protokoll Generierung ab, die für die Wiedergabe der Protokolle erforderlich ist. In der Regel die Prüf Punkt Generierung.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577443(v=exchg.10).md">lgposattach</a></td>
<td>Ruft die LGPOs des letzten Anfügens ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh163307(v=exchg.10).md">lgposkonsistent</a></td>
<td>Ruft die LGPOs ab, wenn die Datenbank konsistent gemacht wurde. Dieser Wert ist NULL, wenn die Datenbank inkonsistent ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566733(v=exchg.10).md">lgposdetach</a></td>
<td>Ruft die LGPOs des letzten detachs ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh564456(v=exchg.10).md">logtimeattach</a></td>
<td>Ruft den Zeitpunkt ab, an dem die Datenbank angefügt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566711(v=exchg.10).md">logtimebadchecksum</a></td>
<td>Ruft den Zeitpunkt ab, zu dem ein nicht korrigier barer Prüfsummen Fehler zuletzt gefunden wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557946(v=exchg.10).md">logtimekonsistent</a></td>
<td>Ruft den Zeitpunkt ab, zu dem die Datenbank konsistent gemacht wurde. Dieser Wert ist NULL, wenn die Datenbank inkonsistent ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh556940(v=exchg.10).md">logtimedetach</a></td>
<td>Ruft die Uhrzeit der letzten Trennung ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557356(v=exchg.10).md">logtimeeccfixfail</a></td>
<td>Ruft den Zeitpunkt der letzten Fehlermeldung ab, die nicht korrigiert werden konnte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578967(v=exchg.10).md">logtimeeccfixsuccess</a></td>
<td>Ruft den Zeitpunkt ab, zu dem der letzte Fehler erfolgreich korrigiert wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577625(v=exchg.10).md">logtimegenmaxcreate</a></td>
<td>Ruft die Erstellungszeit der <a href="hh579109(v=exchg.10).md">genmaxrequired</a> -Protokolldatei ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh579510(v=exchg.10).md">logtimerepair</a></td>
<td>Ruft den letzten Zeitpunkt ab, zu dem die Reparatur für diese Datenbank ausgeführt wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565142(v=exchg.10).md">lspnumber</a></td>
<td>Ruft die Service Pack-Nummer des Betriebssystems aus dem letzten anfügen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh564996(v=exchg.10).md">signdb</a></td>
<td>Ruft die Daten Bank Signatur ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578351(v=exchg.10).md">signlog</a></td>
<td>Ruft die Protokolldatei Signatur von Protokollen ab, die zum Ändern der Datenbank verwendet werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596347(v=exchg.10).md">ulbadchecksum</a></td>
<td>Ruft ab, wie oft ein nicht korrigier barer Prüfsummen Fehler gefunden wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557876(v=exchg.10).md">ulbadchecksumold</a></td>
<td>Ruft ab, wie oft ein nicht korrigier barer Prüfsummen Fehler vor der letzten Reparatur gefunden wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566254(v=exchg.10).md">uleccfixfail</a></td>
<td>Ruft ab, wie oft ein nicht korrigier barer 1-Bit-Fehler aufgetreten ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh564490(v=exchg.10).md">uleccfixfailold</a></td>
<td>Ruft ab, wie oft ein nicht korrigier barer 1-Bit-Fehler aufgetreten ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578574(v=exchg.10).md">uleccfixsuccess</a></td>
<td>Ruft ab, wie oft ein Fehler mit einem Bit erfolgreich korrigiert wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578638(v=exchg.10).md">uleccfixerfolgreiches verkauft</a></td>
<td>Ruft ab, wie oft ein Bit-Fehler vor der letzten Reparatur erfolgreich korrigiert wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh579357(v=exchg.10).md">ulrepairren count</a></td>
<td>Ruft ab, wie oft die Reparatur für diese Datenbank aufgerufen wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557020(v=exchg.10).md">ulrepaungräfin</a></td>
<td>Ruft ab, wie oft diese Datenbank vor der letzten decofragmentierung repariert wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596219(v=exchg.10).md">ulupdate</a></td>
<td>Ruft die inkrementelle Version von ESENT ab, die die Datenbank erstellt hat.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577854(v=exchg.10).md">ulversion</a></td>
<td>Ruft die Version von ESENT ab, von der die Datenbank erstellt wurde.</td>
</tr>
</tbody>
</table>


Oben

## <a name="methods"></a>Methoden

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh557934(v=exchg.10).md">Ist gleich(Objekt)</a></td>
<td>Bestimmt, ob das angegebene <a href="/dotnet/api/system.object">Objekt</a> und das aktuelle- <a href="/dotnet/api/system.object">Objekt</a>gleich sind. (Überschreibt <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. gleich(Objekt)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh565657(v=exchg.10).md">Ist gleich(JET_DBINFOMISC)</a></td>
<td>Gibt an, ob das aktuelle Objekt gleich einem anderen Objekt des gleichen Typs ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh558400(v=exchg.10).md">GetHashCode</a></td>
<td>Gibt den Hashcode für diese Instanz zurück. (Überschreibt <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh556970(v=exchg.10).md">ToString</a></td>
<td>Ruft eine Zeichen folgen Darstellung dieses-Objekts ab. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
