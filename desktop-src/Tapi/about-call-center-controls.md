---
description: TAPI 3 definiert fünf Haupt-ACD-Objekte, die der Agent-Handler der Warteschlange in der Warteschlange für den Agent und die Agentsitzung anlegt. Außerdem wird das TAPI-Objekt mit einer zusätzlichen Schnittstelle ittapicallcenter erweitert.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: Informationen zu Callcenter-Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131645"
---
# <a name="about-call-center-controls"></a>Informationen zu Callcenter-Steuerelementen

TAPI 3 definiert fünf Haupt-ACD-Objekte: den Agent-Handler, die Warteschlange, die ACD-Gruppe, den Agent und die Agentsitzung. Außerdem wird das TAPI-Objekt mit einer zusätzlichen Schnittstelle erweitert – [**ittapicallcenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Agent-Objekt

Das-Agent-Objekt stellt einen Agent dar, der Aufrufe verarbeiten können soll. Dabei handelt es sich normalerweise um eine Person, bei der es sich um eine IVR-oder eine andere Kombination von Software und Hardware Agents sind Schlüssel für ein Callcenter. Sie sind dafür verantwortlich, eingehende Anrufe zu empfangen und zu verarbeiten und gleichzeitig ausgehende Aufrufe an Kunden oder Chancen zu tätigen.

In TAPI bezieht sich das Agent-Objekt direkt auf ein Benutzerkonto, um die Kompatibilität mit vorhandenen Legacy Wechsel Systemen zu gewährleisten. Außerdem kann es sein, dass der Agent mit einer Switch-Agent-ID verknüpft ist, um die Kompatibilität mit vorhandenen Legacy Wechsel Systemen zu gewährleisten.

Das Agentobjekt macht die [**itagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) -Schnittstelle verfügbar. Diese Schnittstelle implementiert Methoden, die eine Agentsitzung erstellen und Statistiken abrufen können, wie z. b. insgesamt behandelte Aufrufe. Anwendungen können das-Agent-Objekt verwenden, um den Agentstatus zu bearbeiten und globale agentstatistiken zu bestimmen.

## <a name="agent-handler-object"></a>Agenthandlerobjekt

Ein Agent-Handler stellt Software oder Hardware dar, die Aufrufe an eine Gruppe von Agents übergeben können. In der Regel handelt es sich hierbei um einen proprietären Switch, der externe Verbindungen mit den Telefonen bei agentstationen verbindet. Die meisten ACD-Systeme verfügen nur über einen solchen Switch, aber große Vorgänge haben möglicherweise mehr. Wenn ein Agent Geräte auf mehr als einem ACD-System hat, wird dem Agent eine entsprechende Anzahl von agenthandlerobjekten angezeigt. Es gibt auch eine Instanz des agentobjekts, die sich auf die Darstellung des Agents in jedem ACD-System bezieht.

Das [**agenthandlerobjekt macht die itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) -Schnittstelle verfügbar. Diese Schnittstelle implementiert Methoden, die Informationen zu den [ACD-Gruppen](#acd-group-object) bereitstellen, die dem Agenthandler und den von ihm verwendeten Adressen zugeordnet sind.

## <a name="agent-session-object"></a>Agentsitzungsobjekt

Eine Agent-Sitzung stellt einen Agent dar, der sich angemeldet hat und für die Handhabung von Aufrufen für eine bestimmte [ACD-Gruppe](#acd-group-object)qualifiziert ist. Eine Agent-Sitzung ist ein dynamisch erstelltes Objekt, das einen Agent mit einer ACD-Gruppe verknüpft, für die er den Dienst bereitstellt, und auch für die Adresse, an der er Anrufe (Turbo, Station, Telefon usw.) empfängt. Anwendungen können das agentsitzungsobjekt verwenden, um die Agentaktivität innerhalb einer bestimmten ACD-Gruppe zu verfolgen.

Das agentsitzungsobjekt macht die [**itagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) -Schnittstelle verfügbar. Diese Schnittstelle implementiert Methoden, die Informationen wie die durchschnittliche Gesprächszeit für einen Aufruf abrufen können.

## <a name="acd-group-object"></a>ACD-Gruppen Objekt

Eine ACD-Gruppe stellt eine Klasse von Aufrufen dar, die eine bestimmte Art der Behandlung erfordert. Beispielsweise können einige eingehende Aufrufe für das Callcenter einer Bank vorhandene Konten betreffen, und andere können sich auf neue Konten beziehen. Einige Agents verfügen möglicherweise über Fachkenntnisse in beiden Bereichen, aber die meisten sind darauf spezialisiert. ACD-Gruppen werden erstellt, um die einzelnen Arten von Anrufen zu verarbeiten. Eine ACD-Gruppe verfügt über eine oder mehrere Warteschlangen. Wenn eingehende Aufrufe klassifiziert werden, werden Sie an Warteschlangen, die der relevanten ACD-Gruppe zugeordnet sind, übermittelt. Ein Aufruf, der aus der Warteschlange stammt, wird an einen Agent übermittelt, der ein [agentsitzungsobjekt](#agent-session-object) erstellt hat, das angibt, dass er Aufrufe von dieser ACD Gruppe verarbeiten kann

Das ACD-Gruppen Objekt macht die [**itacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) -Schnittstelle verfügbar. Diese Schnittstelle implementiert Methoden, die Zugriff auf die Warteschlangen bereitstellen, die der aktuellen ACD-Gruppe zugeordnet sind.

## <a name="queue-object"></a>Queue-Objekt

Das Queue-Objekt stellt einen Punkt innerhalb des ACD-Systems dar, bei dem Aufrufe vorübergehend Ausstehende Aktionen ausgeführt werden. Das Queue-Objekt macht die [**itqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) -Schnittstelle verfügbar. Diese Schnittstelle implementiert Methoden, die Statistiken für eine Warteschlange erfassen, wie z. b. die Anzahl der zurzeit in der Warteschlange Der [ACD-Proxy](acd-proxy.md) verwendet diese Informationen, um Aufrufe an Agents zu verteilen und administrative Berichte zu liefern.

Der Zugriff auf ein Warteschlangen Objekt ermöglicht es einer Anwendung, eine Vielzahl von Standard Statistiken in Bezug auf die Warteschlangen Verwendung zu lesen, aber nicht die Möglichkeit, Aufrufe für die Warteschlange zu steuern. Nur Anwendungen mit Zugriff auf die zugeordneten Adressen und Zeilen (in der Regel die ACD-Proxy Anwendung) können die Aufrufe für die Warteschlange steuern.

Die meisten Warteschlangen beziehen sich direkt auf ein [ACD-Gruppen Objekt](#acd-group-object)und enthalten einen-Rückruf, bis der Agent ihn verarbeiten kann. Es können auch andere Warteschlangen vorhanden sein, um komplexe anführungshandbücher zuzulassen Beispielsweise können Aufrufe in Warteschlangen eingefügt werden, bevor Sie an eine Warteschlange weitergeleitet werden, die von einer ACD-Gruppe bedient wird.

 

 
