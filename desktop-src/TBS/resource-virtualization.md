---
title: Ressourcenvirtualisierung
description: Ressourcenvirtualisierung
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711819"
---
# <a name="resource-virtualization"></a>Ressourcenvirtualisierung

Die primäre Funktion des TSB ist die effiziente Freigabe bestimmter eingeschränkter TPM-Ressourcen: Schlüssel, Autorisierung und Transport Sitzungen.

Wenn eine Instanz einer dieser Ressourcen erstellt wird, erstellt die TSB eine virtuelle Instanz der Ressource und gibt ein Handle für diese virtuelle Instanz im ergebnisbefehlsstream zurück (anstelle der eigentlichen handle-Instanz, die vom TPM zurückgegeben wird). Die TSB verwaltet eine Zuordnung zwischen dem virtuellen Handle und dem eigentlichen handle intern. Wenn das TPM nicht mehr über genügend Speicherplatz verfügt, um mehr Ressourcen eines bestimmten Typs zu speichern, werden vorhandene Instanzen der Ressource selektiv gespeichert und entfernt, bis das TPM die neue Ressource aufnehmen kann. Wenn die alten Ressourcen erneut benötigt werden, lädt die TSB die gespeicherten Kontexte (speichern und auslagern anderer Ressourcen bei Bedarf), bevor der Befehl übermittelt wird.

Die gesamte Virtualisierung in den TSB wird im Auftrag eines bestimmten Kontexts ausgeführt. Jeder Kontext darf nur auf virtuelle Ressourcen zugreifen, die speziell in seinem Namen erstellt wurden, sowie auf die physischen Ressourcen auf dem TPM, die diesen virtuellen Ressourcen entsprechen. Standardmäßig ist die Gesamtzahl aller virtualisierten Ressourcen auf 500 beschränkt. Diese Nummer kann geändert werden, indem Sie einen **DWORD** -Registrierungs Wert mit dem Namen " **maxresources** " unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **TPM** erstellen oder ändern. Die Ressourcennutzung in Echtzeit-TSB kann mithilfe des Leistungs Monitor Tools zum Nachverfolgen der Anzahl von TSB-Ressourcen beobachtet werden. Diese Einschränkung wurde in Windows 8 und Windows Server 2012 als veraltet eingestuft.

Eingeschränkte TPM-Ressourcen, die nicht von den TSB (z. b. Indikatoren und NV-Speicher) virtualisiert werden, müssen gemeinsam zwischen Software Stapeln gemeinsam genutzt werden.

> [!Note]  
> Diese handle-Virtualisierung bewirkt, dass Befehle, die Schlüssel Handles in der Berechnung von HMAC-Autorisierungs Parametern enthalten, fehlschlagen. Infolgedessen können viele in TPM, Version 1,2, veraltete Befehle nicht von der Anwendungssoftware in der TSB-Umgebung verwendet werden.

 

## <a name="resource-limits"></a>Ressourceneinschränkungen

Das TPM ermöglicht es Aufrufern, ihre Funktionen abzufragen, um zu bestimmen, wie viel Speicherplatz für bestimmte Ressourcentypen verfügbar ist. Einige dieser Ressourcen Limits, wie z. b. der verfügbare Speicherplatz für Schlüssel, Autorisierungs Sitzungen und Transport Sitzungen, werden durch die Virtualisierung effektiv durch die TSB erweitert. TSB-Einschränkungen, die von der **maxresources** -Registrierungs Einstellung gesteuert werden, sind in der Regel weitaus größer als die tatsächlichen Einschränkungen der zugrunde liegenden TPM-Hardware. Es wird kein Mechanismus zum Abfragen von TSB-Einschränkungen getrennt von den TPM-Hardware Limits bereitgestellt. Diese TSB-Einschränkung wurde mit Windows 8 und Windows Server 2012 als veraltet eingestuft.

## <a name="keys"></a>Schlüssel

Die TSB virtualisiert Schlüssel Handles, sodass Schlüssel transparent aus dem TPM entladen werden können, wenn Sie nicht verwendet werden und bei Bedarf wieder auf das TPM geladen werden. Wenn ein Schlüssel erstellt wird, ordnet die TSB ein virtuelles handle dem geladenen Schlüssel zu. Das gleiche virtuelle Handle wird für die Lebensdauer der Ressource verwendet. Virtuelle Schlüssel Handles sind nur in dem Kontext gültig, in dem Sie erstellt wurden, und die zugeordneten Ressourcen werden über die Lebensdauer des Kontexts hinaus nicht beibehalten.

-   Erstellen von Schlüsseln mit TPM \_ LoadKey2

    Wenn ein Schlüssel mit dem TPM-LoadKey2, dem TPM2-Befehl "", dem \_ \_ Befehl "TPM2 Load" oder dem \_ TPM2 \_ loadexternal-Befehl erstellt wird, ersetzt die TSB das Handle im Rückgabe Byte-Stream durch ein virtuelles Schlüssel handle seiner Wahl. Folglich stellt die TSB sicher, dass jedes virtuelle handle eindeutig ist. Wenn die TSB eine Kollision erkennt (ein äußerst unwahrscheinliches Ereignis), entlädt die TSB den Schlüssel vom TPM und informiert die aufrufende Software. Die Software kann den Vorgang dann erneut übermitteln. Dieser Vorgang kann wiederholt werden, bis die TSB ein eindeutiges Schlüssel handle erhält.

-   Löschen von Schlüsseln

    Der TSB macht das virtuelle Schlüssel Handle für ungültig, wenn es eine TPM- \_ flushspecific-oder TPM2 \_ flushcontext-Nachricht für dieses virtuelle Handle aus dem Client Kontext empfängt. Wenn der Schlüssel im TPM physisch vorhanden ist, wenn die Leerungs Nachricht empfangen wird, leert die TSB den Schlüssel zu diesem Zeitpunkt aus dem TPM.

-   Temporäres Entfernen von Schlüsseln

    Wenn Sie einen Schlüssel aus dem TPM entfernen, um Platz für ein neues Element zu schaffen, führt die TSB einen TPM \_ savecontext-oder TPM2 \_ contextsave-Befehl für den Schlüssel aus, bevor Sie ihn entfernen.

-   Wiederherstellen von Schlüsseln

    Wenn ein Befehl, der auf einen geladenen Schlüssel verweist, an den TSB übermittelt wird, wird sichergestellt, dass der Schlüssel physisch auf dem TPM vorhanden ist. Wenn der Schlüssel nicht vorhanden ist, stellt der TSB ihn mit einem TPM- \_ loadcontext oder TPM2 \_ contextload wieder her. Wenn ein Schlüssel nicht auf dem TPM wieder hergestellt werden kann, gibt TSB ein \_ \_ ungültiges \_ keyHandle als TPM-Ergebnis zurück.

Die TSB ersetzt jedes virtuelle handle, das einem Schlüssel in einem Befehlsdaten Strom zugeordnet ist, durch das physische Handle des Schlüssels, der auf dem TPM geladen wurde. Wenn ein Befehl mit einem virtuellen handle übermittelt wird, das von den TSB nicht im Kontext des Aufrufers erkannt wird, formatiert TSB einen fehlerstream für den Aufrufer mit einem \_ \_ ungültigen keyHandle von TPM E \_ .

## <a name="authorization-sessions"></a>Autorisierungs Sitzungen

Autorisierungs Sitzungen werden durch Aufrufen von TPM \_ OIAP, TPM \_ OSAP oder TPM \_ DSAP erstellt. In jedem Fall enthält der Rückgabe Byte Datenstrom das physische TPM-Handle der neu erstellten Autorisierungs Sitzung. Die TSB ersetzt dies durch ein virtuelles handle. Beim anschließenden Verweis auf die Autorisierungs Sitzung ersetzt die TSB das virtuelle Handle im Befehlsdaten Strom durch das physische Handle der Autorisierungs Sitzung. Die TSB stellt sicher, dass die Lebensdauer der virtuellen Autorisierungs Sitzung mit der der physischen Autorisierungs Sitzung übereinstimmt. Wenn ein Client versucht, ein abgelaufenes virtuelles Handle zu verwenden, formatiert TSB einen Fehler Datenstrom mit dem Fehler TPM \_ invalidauthhandle.

Sitzungs Slots sind begrenzt, und die TSB kann aus externen Slots bestehen, in denen Sie Autorisierungs Sitzungs Kontexte speichern können. In diesem Fall wählt die TSB eine Autorisierungs Sitzung aus, die für ungültig erklärt werden soll, damit der neue Kontext erfolgreich gespeichert werden kann. Eine Anwendung, die versucht, den alten Kontext zu verwenden, muss die Autorisierungs Sitzung neu erstellen.

Der TSB macht die virtuelle Autorisierungs Sitzung ungültig, wenn einer der folgenden Fälle eintritt:

-   Das Flag für die Fortsetzung der Verwendung, das der Autorisierungs Sitzung im zurückgegebenen Befehlsdaten Strom vom TPM zugeordnet ist, ist **false**.
-   Ein Befehl, der eine Autorisierungs Sitzung verwendet, schlägt fehl.
-   Ein Befehl wird ausgeführt, der die mit dem Befehl verknüpfte Autorisierungs Sitzung (z. b. TPM-Aufforderungs Schlüssel) für ungültig erklärt \_ .
-   Ein Schlüssel, der einer OSAP-oder DSAP-Sitzung zugeordnet ist, wird durch einen Aufrufen von TPM \_ flushspecific oder TPM2 flushcontext aus dem TPM entfernt \_ (ohne Rücksicht darauf, ob dieser Befehl aus dem TSB oder mit einer höheren Software stammt).

    Die TSB synchronisiert die Autorisierungs Sitzungen nach erfolgreicher Ausführung bestimmter nicht deterministischer Befehle automatisch erneut, um sicherzustellen, dass der TSB-Status mit dem TPM-Status konsistent bleibt. Die folgenden Befehle sind betroffen:

    -   TPM Ord-Delegat \_ \_ \_ Verwalten
    -   TPM Ord-Delegat " \_ \_ \_ kreatebesitzdelegation"
    -   TPM \_ Ord Delegat \_ \_ loadbesitzdelegierung

In jedem der folgenden Fälle wird die Autorisierungs Sitzung auf dem TPM automatisch vom TPM geleert:

-   Erstellen von Autorisierungs Sitzungen

    Die Sitzungs Handles der virtuellen Autorisierung sind nur im Kontext gültig, in dem Sie erstellt wurden, und die zugeordneten Ressourcen werden über die Lebensdauer des zugeordneten Kontexts hinaus nicht beibehalten.

-   Löschen von Autorisierungs Sitzungen

    Der TSB macht die virtuelle Autorisierungs Sitzung ungültig, wenn er einen TPM- \_ flushspecific-oder TPM2 \_ flushcontext-Befehl für das virtuelle Handle aus dem Client Kontext empfängt. Wenn die Autorisierungs Sitzung auf dem TPM physisch vorhanden ist, wenn der Flush-Befehl empfangen wird, leert die TSB die physische Sitzung sofort vom TPM.

-   Temporäres Entfernen von Autorisierungs Sitzungen

    Wenn Sie eine Autorisierungs Sitzung aus dem TPM entfernen, um Platz für eine neue Entität zu schaffen, führt die TSB TPM \_ savecontext oder TPM2 \_ contextsave in dieser Autorisierungs Sitzung aus.

-   Autorisierungs Sitzungen

    Wenn ein autorisierter TPM-Befehl an die TSB übermittelt wird, stellt die TSB sicher, dass alle virtuellen Autorisierungs Sitzungen, auf die im Befehl verwiesen wird, physisch auf dem TPM vorhanden sind. Wenn eine der Autorisierungs Sitzungen nicht vorhanden ist, stellt die TSB Sie mit einem TPM- \_ loadcontext oder TPM2 \_ contextload wieder her. Wenn eine Autorisierungs Sitzung nicht auf dem TPM wieder hergestellt werden kann, gibt die TSB ein \_ Ungültiges Handle von TPM E \_ \_ als TPM-Ergebnis zurück.

Die TSB ersetzt alle virtuellen Handles, die einer Autorisierungs Sitzung in einem Befehlsdaten Strom zugeordnet sind, durch das physische Handle der Autorisierungs Sitzung, die auf dem TPM geladen wurde.

Wenn ein Befehl mit einem virtuellen handle übermittelt wird, das von den TSB nicht im Kontext des Aufrufers erkannt wird, formatiert TB einen Fehler Datenstrom für den Aufrufer mit dem Fehler TPM \_ E \_ ungültiges \_ handle.

## <a name="transport-sessions"></a>Transport Sitzungen

> [!Note]  
> Die Verarbeitung von Transport Sitzungen, wie hier beschrieben, ist spezifisch für Windows Vista und Windows Server 2008.

 

Transport Sitzungen sind ein Mechanismus, der vom TPM bereitgestellt wird, das es einem Software Stapel ermöglicht, Daten in einem Befehl bei der Übertragung zwischen der Software und dem TPM zu verschlüsseln. Dadurch wird verhindert, dass ein Angreifer die Daten abfängt, während er den Hardware Bus übergibt.

> [!IMPORTANT]
> Nur die Nutzlastdaten werden verschlüsselt. Die ausgeführten Befehle können weiterhin identifiziert werden.

 

Leider verhindert dieser Mechanismus auch, dass die TSB Nutzlastdaten untersucht. In den meisten Fällen ist dies kein Problem, da die TSB nur Handles, keine Nutzlastdaten, ändert. Im Fall von TPM \_ loadcontext wird das zurückgegebene Ressourcen handle jedoch durch die Verschlüsselung abgedeckt. Daher verhindert die TSB Versuche, einen TPM \_ loadcontext-Vorgang auszuführen, der von einer Transport Sitzung abgedeckt wird.

Die TSB blockiert die folgenden Befehle unter Transport Sitzung:

-   TPM- \_ integrishtransport
-   TPM- \_ executetransport
-   TPM-Beendigungs \_ \_ handle
-   TPM- \_ loadkey
-   TPM \_ evictkey
-   TPM \_ savekeycontext
-   TPM \_ loadkeycontext
-   TPM \_ saveauthcontext
-   TPM \_ loadauthcontext
-   TPM \_ savecontext
-   TPM- \_ loadcontext
-   TPM \_ flushspecific

Wenn einer dieser Befehle durch eine Transport Sitzung abgedeckt ist, wird der TPM E Embedded-Befehl von TSB \_ \_ \_ \_ als TPM-Ergebnis nicht unterstützt zurückgegeben.

Transport Sitzungs Handles werden ähnlich wie Schlüssel Handles und Autorisierungs Handles virtualisiert. Es ist eine begrenzte Anzahl gespeicherter Kontext Slots für die Transport Sitzung auf dem TPM verfügbar.

Der TSB macht die virtuelle Transport Sitzung ungültig, wenn einer der folgenden Fälle eintritt:

-   Das Flag für die Fortsetzung der Verwendung, das der Transport Sitzung im Rückgabe Befehlsstream aus dem TPM zugeordnet ist, ist **false**.

    Wie bei den obigen Autorisierungs Sitzungen werden Transport Sitzungen von TSB nach erfolgreicher Ausführung bestimmter nicht deterministischer Befehle automatisch erneut synchronisiert, um sicherzustellen, dass der TSB-Status mit dem TPM-Status konsistent bleibt. Die folgenden Befehle sind betroffen:

    -   TPM Ord-Delegat \_ \_ \_ Verwalten
    -   TPM Ord-Delegat " \_ \_ \_ kreatebesitzdelegation"
    -   TPM \_ Ord Delegat \_ \_ loadbesitzdelegierung

In jedem dieser Fälle wird die Transport Sitzung auf dem TPM automatisch vom TPM geleert:

-   Erstellen von Transport Sitzungen

    Die TSB erstellt ein virtuelles Handle für jede Transport Sitzung, die von einem Client erstellt wurde. Virtuelle Transport Handles sind nur in dem Kontext gültig, in dem Sie erstellt wurden, und die zugeordneten Ressourcen werden über die Lebensdauer des zugeordneten Kontexts hinaus nicht beibehalten.

-   Löschen von Transport Sitzungen

    Der TSB macht die virtuelle Transport Sitzung ungültig, wenn er einen TPM- \_ flushspecific-Befehl für das virtuelle Handle aus dem Client Kontext empfängt. Wenn die Transport Sitzung auf dem TPM physisch vorhanden ist, wenn der Flush-Befehl empfangen wird, leert die TSB die physische Sitzung sofort vom TPM.

-   Temporäres Entfernen von Transport Sitzungen

    Wenn Sie eine Transport Sitzung aus dem TPM entfernen, um Platz für eine neue Entität zu schaffen, führt TSB den TPM \_ savecontext in dieser Transport Sitzung aus.

-   Wiederherstellen von Transport Sitzungen

    Wenn ein TPM- \_ Befehl executetransport an den TSB übermittelt wird, stellt die TSB sicher, dass die Transport Sitzung, auf die im Befehl verwiesen wird, physisch auf dem TPM vorhanden ist. Wenn die Transport Sitzung nicht vorhanden ist, wird Sie von TSB mit einem TPM-loadcontext-Rückruf wieder hergestellt \_ .

Der TSB ersetzt das virtuelle handle, das der Transport Sitzung in einem Befehlsdaten Strom zugeordnet ist, durch das physische Handle der auf dem TPM geladenen Transport Sitzung. Wenn ein Befehl mit einem virtuellen handle übermittelt wird, das von den TSB nicht im Kontext des Aufrufers erkannt wird, formatiert TB einen Fehler Datenstrom für den Aufrufer mit einem ungültigen Handle von TPM \_ E \_ \_ .

## <a name="exclusive-transport-sessions"></a>Exklusive Transport Sitzungen

Exklusive umschließende Transport Sitzungen sind eine Möglichkeit für Software auf oberster Ebene, um zu bestimmen, ob eine andere Software während einer Kette von Befehlen auf das TPM zugegriffen hat. Sie verhindern nicht, dass andere Software auf das TPM zugreift, sondern nur dem Ersteller der Transport Sitzung eine Möglichkeit zur Bestimmung, dass ein anderer Zugriff aufgetreten ist. Die TSB führt keine spezifischen Aktionen aus, um exklusive Transport Sitzungen zu behindern, aber Sie ist mit Ihnen nicht kompatibel. Die TSB versucht, das natürliche Verhalten des TPM zu duplizieren, indem Sie transparent ist, sodass keine Befehle aus Kontexten bevorzugt werden, die eine exklusive Transport Sitzung einrichten. Wenn z. B. Client B einen Befehl übermittelt, wenn sich Client a in einer exklusiven Transport Sitzung befindet, wird die exklusive Transport Sitzung von Client a ungültig.

Von TSB initiierte Befehle können auch die exklusive Transport Sitzung beenden. Dies ist der Fall, wenn sich Client a in einer exklusiven Transport Sitzung befindet und ein von Client a ausgeführter Befehl eine Ressource aufruft, die im TPM nicht physisch vorhanden ist. Diese Situation bewirkt, dass der TSB-Virtualisierungs-Manager einen TPM \_ loadcontext-Befehl ausführt, um diese Ressource bereitzustellen, wodurch die exklusive Transport Sitzung von Client a beendet wird.

 

 




