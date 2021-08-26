---
title: Sensorpools
description: 'Beschreibt drei mögliche Sensorpoolsysteme: "Privat" und "Nicht zugewiesen".'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d28bd03d84e2558f0fb1ba090440aa2bda62292c51773d54d5094466ba9e494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035260"
---
# <a name="sensor-pools"></a>Sensorpools

Zur Unterstützung Windows Authentifizierungsszenarien und der vom Anbieter definierten Authentifizierung organisiert der Windows Biometrische Dienst biometrische Einheiten in drei mögliche Sensorpools:

-   **Privater Pool:** Sammlung biometrischer Einheiten, die für die exklusive Verwendung durch eine Clientanwendung zugeordnet sind. Private Pools können Authentifizierungsszenarien unterstützen, die nicht Windows-basiert sind, und ermöglichen es einer Anwendung, auf die Hardware einer biometrischen Einheit auf anbieterdefinierte Weise zu zugreifen. Das System kann so viele private Sensorpools wie biometrische Einheiten haben.
-   **Systemsensorpool:** Sammlung von sharable-biometrischen Einheiten, die Zugriff auf Windows Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und jedem anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zu ordnet. Jeder biometrische Dienstanbieter verfügt über einen Systemsensorpool.
-   **Nicht zugewiesener Pool** enthält eine (möglicherweise leere) Sammlung biometrischer Einheiten, die weder dem Systempool noch dem privaten Pool zugewiesen sind.

Anwendungen können den freigegebenen Systempool verwenden oder einen privaten Pool erstellen, der aus biometrischen Einheiten besteht, die aus dem System oder nicht zugewiesenen Pools entfernt wurden. Wenn eine Anwendung ihren privaten Pool frei gibt, werden die biometrischen Einheiten neu konfiguriert und an ihre ursprünglichen Pools zurückgegeben. Um Denial-of-Service-Angriffe zu verhindern, dürfen nur privilegierte Benutzer den letzten Sensor aus dem Systempool entfernen. Weitere Informationen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Privater Sensorpool](private-sensor-pool.md)<br/>   | Eine Sammlung biometrischer Einheiten, die für die exklusive Verwendung durch eine Clientanwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen einer Clientanwendung den Zugriff auf eine biometrische Einheit mithilfe von vom Anbieter angegebenen Steuerungsbefehlen.<br/> |
| [Systemsensorpool](system-sensor-pool.md)<br/>     | Eine Sammlung von sharable-biometrischen Einheiten, die Zugriff auf Windows Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und jedem anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zu ordnet.<br/>                                 |
| [Systempoolverhalten](system-pool-behavior.md)<br/> | Diskussion über die Aktionen, die vom Systempool durchgeführt werden, wenn Ereignisbenachrichtigungen gesendet werden und keine biometrischen Vorgänge ausstehen.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Windows Biometrieframework-API](./biometric-service-api-portal.md)
</dt> </dl>

 

