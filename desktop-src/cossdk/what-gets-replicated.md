---
description: Was wird repliziert?
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Was wird repliziert?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60b08151c14d0254bd856fe2ee5b7b83d85714d1b435a32817bf66cc11a1e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636650"
---
# <a name="what-gets-replicated"></a>Was wird repliziert?

## <a name="applications"></a>Anwendungen

Alle auf dem Quellcomputer installierten Anwendungen werden repliziert, mit Ausnahme der folgenden:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Nicht-COM+-Anwendungselemente und -Abhängigkeiten
</dt> <dd>

Der Administrator ist für die Replikation aller Daten verantwortlich, von denen eine COM+-Anwendung abhängt, die jedoch nicht ordnungsgemäß Teil der Anwendung selbst ist, z. B. Datendateien und DLLs. COMREPL repliziert nichts außerhalb von COM+-Anwendungselementen.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Vorinstallierte COM+-Anwendungen
</dt> <dd>

Anwendungen, die intern von COM+ verwendet und über das COM+-Setupprogramm installiert werden, werden nicht repliziert. Dabei handelt es sich z. B. um:

-   Systemanwendung
-   COM+-Hilfsprogramme
-   COM+ QC Dead Letter Queue Listener

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Von IIS erstellte Anwendungen
</dt> <dd>

Diese Anwendungen werden nicht repliziert und umfassen Folgendes:

-   IIS-In-Process-Anwendungen
-   IIS-Hilfsprogramme
-   Alle Anwendungen, die für isolierte oder gepoolte virtuelle Stämme erstellt wurden

</dd> </dl>

## <a name="computer-list"></a>Computerliste

Die Remotecomputer, die im Ordner **Computer** im Verwaltungstool komponentendienste genannt werden, werden nicht vom Quell- zum Zielcomputer repliziert.

## <a name="properties"></a>Eigenschaften

Die folgenden **LocalComputer-Sammlungseigenschaften** werden repliziert:

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   Ports
-   RpcProxyEnabled

Die folgenden **LocalComputer-Sammlungseigenschaften** werden nicht repliziert:

-   Beschreibung
-   ApplicationProxyRSN
-   IsRouter

Beschreibungen der **LocalComputer-Sammlungseigenschaften** finden Sie unter [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikationsphasen](replication-phases.md)
</dt> <dt>

[Verwenden von COMREPL](using-comrepl.md)
</dt> </dl>

 

 



