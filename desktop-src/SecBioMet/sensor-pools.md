---
title: Sensor Pools
description: Beschreibt drei mögliche Sensor Pools System, private und nicht zugewiesene.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390553"
---
# <a name="sensor-pools"></a>Sensor Pools

Zur Unterstützung von Windows-Authentifizierungs Szenarien und Hersteller definierter Authentifizierung organisiert der Windows-biometrische Dienst biometrische Einheiten in drei mögliche Sensor Pools:

-   **Privater Pool** eine Sammlung von biometrischen Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert werden. Private Pools können Authentifizierungs Szenarien unterstützen, die nicht auf Windows basieren, und eine Anwendung können auf die Hardware einer biometrischen Einheit auf Hersteller definierte Weise zugreifen. Es können beliebig viele private Sensor Pools auf dem System vorhanden sein, da biometrische Einheiten vorhanden sind.
-   **System Sensor Pool** : eine Sammlung von shardbaren biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet. Jeder biometrische Dienstanbieter verfügt über einen System Sensor Pool.
-   **Nicht zugewiesener Pool** enthält eine (möglicherweise leere) Auflistung von biometrischen Einheiten, die weder dem System Pool noch dem privaten Pool zugewiesen sind.

Anwendungen können den freigegebenen System Pool verwenden, oder Sie können einen privaten Pool erstellen, der aus biometrischen Einheiten besteht, die aus dem System oder aus nicht zugewiesenen Pools entfernt wurden. Wenn eine Anwendung Ihren privaten Pool freigibt, werden die biometrischen Einheiten neu konfiguriert und an Ihre ursprünglichen Pools zurückgegeben. Um Denial-of-Service-Angriffe zu verhindern, dürfen nur privilegierte Benutzer den letzten Sensor aus dem System Pool entfernen. Weitere Informationen finden Sie in den nachfolgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Privater Sensor Pool](private-sensor-pool.md)<br/>   | Eine Sammlung biometrischer Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert sind. Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen es einer Client Anwendung, mithilfe von vom Hersteller angegebenen Steuerungs Befehlen auf eine biometrische Einheit zuzugreifen.<br/> |
| [System Sensor Pool](system-sensor-pool.md)<br/>     | Eine Auflistung von freigegeben-biometrischen Einheiten, die Zugriff auf die Windows-Authentifizierungsdienste bieten. Dieser Pool wird von Winlogon, UAC und einem beliebigen anderen Client verwendet, der einer bestimmten biometrischen Vorlage eine SID zuordnet.<br/>                                 |
| [System Pool Verhalten](system-pool-behavior.md)<br/> | Erörterung der Aktionen, die vom System Pool durchgeführt werden, wenn Ereignis Hinweise gesendet werden und keine biometrischen Vorgänge ausstehen.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Windows-Biometrieframework-API](./biometric-service-api-portal.md)
</dt> </dl>

 

