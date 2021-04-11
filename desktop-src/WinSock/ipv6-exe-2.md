---
description: Alle IPv6-Konfigurationen werden mit dem Ipv6.exe-Tool ausgeführt.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214590"
---
# <a name="ipv6exe"></a>Ipv6.exe

Alle IPv6-Konfigurationen werden mit dem Ipv6.exe-Tool ausgeführt. Dieses Tool wird hauptsächlich zum Abfragen und Konfigurieren von IPv6-Schnittstellen, Adressen, Caches und Routen verwendet. Im folgenden finden Sie IPv6-Unterbefehle:

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 if** \[ sei\#\]
</dt> <dd>

Zeigt Informationen über Schnittstellen an. Wenn eine Schnittstellen Nummer angegeben ist, werden nur Informationen zu dieser Schnittstelle angezeigt. Andernfalls werden Informationen zu allen Schnittstellen angezeigt. Die Ausgabe enthält die Verknüpfungs Schicht Adresse der Schnittstelle und die Liste der IPv6-Adressen, die der Schnittstelle zugewiesen sind, einschließlich der aktuellen MTU der Schnittstelle und der maximalen (echten) MTU, die von der Schnittstelle unterstützt werden kann.

Schnittstelle \# 1 ist eine für Loopback verwendete Pseudo Schnittstelle. Schnittstelle \# 2 ist eine Pseudo Schnittstelle für konfigurierte Tunnelung, automatische Tunnelung und IPv6-zu-IPv4-Tunnelung. Andere Schnittstellen werden sequenziell in der Reihenfolge nummeriert, in der Sie erstellt werden. Diese Bestellung variiert von einem Computer zu einem anderen.

Adressen der Verknüpfungs Schicht im *AA* - *BB* - *CC* - *DD* - *EE* - *FF* -Format sind Ethernet-Adressen. Die Adresse der Verknüpfungs Schicht in *einer*. *b*. *c*. Das *d* -Formular ist 6-over-4-Schnittstellen. Weitere Informationen zu 6-over-4 finden Sie unter RFC 2529.

Die beiden Pseudo Schnittstellen verwenden keine IPv6-Nachbar Ermittlung.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6** -"IFC", wenn "Weiterleiten" angekündigt-weiterleitet: gibt den \# \[ \] \[ \] \[ \] \[ \] \[ \# \] \[ Standort Bezeichner der MTU-\]
</dt> <dd>

Steuert Schnittstellen Attribute. Schnittstellen können weitergeleitet werden. in diesem Fall leiten Sie Pakete mit Zieladressen weiter, die nicht der Schnittstelle zugewiesen sind. Schnittstellen können Werbung sein. in diesem Fall senden Sie Routerankündigungen. Diese Attribute können unabhängig voneinander gesteuert werden. Eine Schnittstelle sendet entweder routerzuweisungen und empfängt Routerankündigungen, oder Sie empfängt routerzuweisungen und sendet Routerankündigungen.

Da die beiden Pseudo Schnittstellen keine Nachbar Ermittlung verwenden, können Sie nicht für das Senden von Routerankündigungen konfiguriert werden.

Weiterleitungen können als FORW abgekürzt und als ADV angekündigt werden.

Die MTU für die Schnittstelle kann auch festgelegt werden. Die neue MTU muss kleiner oder gleich der maximalen (von IPv6 gemeldeten) MTU (wie von IPv6) und größer oder gleich der minimalen IPv6-MTU (1280 Bytes) sein.

Der Standort Bezeichner für eine Schnittstelle kann ebenfalls geändert werden. Website \_ Bezeichner werden im Feld sin6 Scope \_ ID mit Site-Local-Adressen verwendet.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IPv6-IFD** , wenn\#
</dt> <dd>

Löscht eine Schnittstelle. Die Loopback-und Tunnel Pseudo Schnittstellen können nicht gelöscht werden.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**IPv6-NC** \[ If- \# \[ Adresse\]\]
</dt> <dd>

Zeigt den Inhalt des Nachbar Caches an. Wenn eine Schnittstellen Nummer angegeben ist, wird nur der Inhalt des Nachbar Caches dieser Schnittstelle angezeigt. Andernfalls werden die Inhalte der Nachbar Caches aller Schnittstellen angezeigt. Wenn eine Schnittstelle angegeben ist, kann eine IPv6-Adresse angegeben werden, um nur diesen Nachbar Cache Eintrag anzuzeigen.

Für jeden Nachbar Cache Eintrag werden die Schnittstelle, die IPv6-Adresse, die Adresse der Verbindungsschicht und der Status REACH angezeigt.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**IPv6-NCF** \[ If- \# \[ Adresse\]\]
</dt> <dd>

Leert die angegebenen Nachbar Cache Einträge. Nur benachbarte Cache Einträge ohne Verweise werden gelöscht. Da Routen Cache Einträge Verweise auf Nachbar Cache Einträge enthalten, sollte der Routen Cache zuerst geleert werden. Routing Tabelleneinträge können auch Verweise auf Nachbar Cache Einträge enthalten.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**IPv6 RC** \[ If- \# Adresse\]
</dt> <dd>

Zeigt den Inhalt des Routen Caches an. Der Routen Cache ist der Name der Microsoft IPv6-Implementierung für den Zielcache. Wenn eine Schnittstelle und eine Adresse angegeben werden, wird der Routen Cache Eintrag zum Erreichen der Adresse über die Schnittstelle angezeigt. Andernfalls werden alle Routen Cache Einträge angezeigt.

Für jeden Routen Cache Eintrag werden die IPv6-Adresse und die aktuelle Schnittstelle für den nächsten Hop und die Nachbaradresse angezeigt. Die bevorzugte Quelladresse für die Verwendung mit diesem Ziel, der aktuelle Pfad der MTU zum Erreichen dieses Ziels über die-Schnittstelle und die Bestimmung, ob dies ein Schnittstellen spezifischer –-Routen Cache Eintrag ist. Eine beliebige Adresse (für Mobilität) für die Zieladresse wird ebenfalls angezeigt.

Eine Zieladresse kann mehrere Routen Cache Einträge aufweisen – so viele wie eine für jede ausgehende Schnittstelle. Eine Zieladresse kann jedoch maximal einen Routen Cache Eintrag aufweisen, der nicht Schnittstellen spezifisch ist. Ein Schnittstellen spezifischer –-Routen Cache Eintrag wird nur verwendet, wenn die Anwendung explizit diese ausgehende Schnittstelle angibt.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**IPv6-RCF** \[ If- \# \[ Adresse\]\]
</dt> <dd>

Leert die angegebenen Routen Cache Einträge.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**IPv6-BC**
</dt> <dd>

Zeigt den Inhalt des Bindungs Caches an, der Bindungen zwischen Privatadressen und Pflege Adressen für mobile IPv6 enthält.

Für jede Bindung werden die Privatadresse, die Adresse, die Bindungs Sequenznummer und die Lebensdauer angezeigt.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 Adu** if \# /Address \[ Lifetime VL \[ "/pl" \] \] \[ Anycast \] \[ Unicast\]
</dt> <dd>

Fügt eine Unicast-oder Anycast-Adresszuweisung zu einer Schnittstelle hinzu oder entfernt Sie. Die Unicastadresse wird befolgt, es sei denn, es wurde Anycast angegeben.

Die Lebensdauer ist unendlich, wenn nicht angegeben. Wenn nur eine gültige Gültigkeitsdauer angegeben wird, ist die bevorzugte Lebensdauer gleich der gültigen Gültigkeitsdauer. Es kann eine unendliche Lebensdauer oder ein endlicher Wert in Sekunden angegeben werden. Die bevorzugte Lebensdauer muss kleiner oder gleich der gültigen Gültigkeitsdauer sein. Die Angabe einer Lebensdauer von NULL bewirkt, dass die Adresse entfernt wird.

Sie können die Lebensdauer als Lebensdauer abkürzen.

Bei Anycast-Adressen sind die einzigen gültigen Gültigkeitsdauer Werte 0 (null) und unendlich.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**IPv6-SPT**
</dt> <dd>

Zeigt den aktuellen Inhalt der Site-Präfix Tabelle an.

Für jedes Site Präfix zeigt der Befehl das Präfix, die Schnittstelle, für die das Site Präfix gilt, und die Präfix Lebensdauer in Sekunden an.

Standort Präfixe werden normalerweise automatisch von Routerankündigungen aus konfiguriert. Sie werden in der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion verwendet, um ungeeignete Site lokale Adressen zu filtern.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**IPv6-SPU** -Präfix bei \# \[ Lebensdauer L\]
</dt> <dd>

Fügt ein Präfix in der Präfix Tabelle der Site hinzu, entfernt oder aktualisiert dieses.

Die Präfix-und Schnittstellen Nummer ist erforderlich. Die Lebensdauer des Standortpräfixes, angegeben in Sekunden, ist standardmäßig unbegrenzt, wenn nichts angegeben ist. Durch die Angabe einer Lebensdauer von NULL wird das Site Präfix gelöscht.

Dieser Befehl ist für die normale Konfiguration von Hosts oder Routern nicht erforderlich.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**IPv6-RT**
</dt> <dd>

Zeigt den aktuellen Inhalt der Routing Tabelle an.

Für jeden Routing Tabelleneintrag zeigt der Befehl das Routen Präfix, eine auf-Link-Schnittstelle oder einen Nachbar für den nächsten Hop auf einer Schnittstelle an, ein bevorzugter Wert (kleiner wird bevorzugt) und eine Lebensdauer in Sekunden.

Routing Tabelleneinträge können auch über **Veröffentlichungs** -und **Alterungs** Attribute verfügen. Standardmäßig werden Sie verwendet (die Lebensdauer wird nicht als verbleibende Konstante angezeigt), und Sie werden nicht veröffentlicht (beim Konstruieren von Routerankündigungen nicht verwendet).

Auf Hosts werden Routing Tabelleneinträge normalerweise automatisch von Routerankündigungen aus konfiguriert.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**IPv6-RTU** -Präfix, wenn \# \[ /nexthop \] \[ Lebensdauer L \] \[ \] \[ \] \[ -Einstellung P \] \[ SPL Site-Prefix-length\]
</dt> <dd>

Fügt eine Route in der Routing Tabelle hinzu oder entfernt Sie. Das Routen Präfix ist erforderlich. Das Präfix kann auf eine angegebene Schnittstelle oder auf den nächsten Hop mit einer Nachbaradresse auf einer Schnittstelle festgelegt werden. Die Route kann eine Lebensdauer in Sekunden aufweisen, mit der Standardeinstellung unendlich und eine Voreinstellung mit dem Standardwert 0 (null) oder am bevorzugten. Wenn Sie die Lebensdauer 0 angeben, wird die Route gelöscht.

Wenn die Route als veröffentlicht angegeben wird, gibt Sie an, dass Sie beim Erstellen von Routerankündigungen verwendet wird. Die Lebensdauer der Route wird nicht nach unten gezählt und ist daher praktisch unendlich, aber der Wert wird in Routerankündigungen verwendet. Optional kann eine Route auch als veröffentlichte Route angegeben werden. Eine nicht veröffentlichte Route ist standardmäßig immer Ages.

Die optionale SPL-unter Option kann verwendet werden, um eine Site Präfix Länge anzugeben, die der Route zugeordnet ist. Die Site Präfix Länge wird nur beim Senden von Routerankündigungen verwendet.

Die Lebensdauer kann als "Life", als "Pref" und als "pub" veröffentlicht werden.

</dd> </dl>

 

 



