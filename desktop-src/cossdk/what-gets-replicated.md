---
description: Was wird repliziert?
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Was wird repliziert?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342768"
---
# <a name="what-gets-replicated"></a>Was wird repliziert?

## <a name="applications"></a>Anwendungen

Alle auf dem Quellcomputer installierten Anwendungen werden mit Ausnahme der folgenden repliziert:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Nicht-com +-Anwendungs Elemente und-Abhängigkeiten
</dt> <dd>

Der Administrator ist dafür verantwortlich, alle Elemente zu replizieren, von denen eine COM+-Anwendung abhängt, die jedoch nicht ordnungsgemäß Teil der Anwendung selbst ist, wie z. b. Datendateien und DLLs. Comrepl repliziert nichts außerhalb der com+-Anwendungs Elemente.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Vorinstallierte com+-Anwendungen
</dt> <dd>

Anwendungen, die intern von com+ verwendet werden und über das com+-Setup Programm installiert werden, werden nicht repliziert. Dabei handelt es sich z. B. um:

-   System Anwendung
-   Com+-Hilfsprogramme
-   Anqueue-Listener für com+-QC

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Von IIS erstellte Anwendungen
</dt> <dd>

Diese Anwendungen werden nicht repliziert und umfassen Folgendes:

-   IIS-in-Process-Anwendungen
-   IIS-Hilfsprogramme
-   Alle Anwendungen, die für isolierte oder gepoolte virtuelle Stämme erstellt wurden

</dd> </dl>

## <a name="computer-list"></a>Computer Liste

Die Remote Computer, die im Ordner " **Computer** " im Verwaltungs Tool "Komponenten Dienste" genannt werden, werden nicht von der Quell-auf den Zielcomputer repliziert.

## <a name="properties"></a>Eigenschaften

Die folgenden **LocalComputer** -Sammlungs Eigenschaften werden repliziert:

-   TransactionTimeout
-   Resourcepoolingenabled
-   Dcomaktiviert
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   Securitytrackingenabled
-   Cisenabled
-   Securereferencesaktiviert
-   Internetportslisted
-   Deafulttinternetports
-   Ports
-   Rpcproxyaktivierte

Die folgenden **LocalComputer** -Sammlungs Eigenschaften werden nicht repliziert:

-   BESCHREIBUNG
-   Applicationproxyrsn
-   Isrouter

Beschreibungen der Eigenschaften der **LocalComputer** -Sammlung finden Sie unter [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikations Phasen](replication-phases.md)
</dt> <dt>

[Verwenden von Comrepl](using-comrepl.md)
</dt> </dl>

 

 



