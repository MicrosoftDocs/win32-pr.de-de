---
title: Schreiben von abwärts kompatiblen Clients und Servern
description: Theoretisch hilft das Versions Schema von RPC dabei, eine Fehlkommunikation zwischen geänderten Servern und Clients und ihren bereitgestellten Gegenstücken zu verhindern.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, Abwärtskompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100666"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Schreiben von abwärts kompatiblen Clients und Servern

Theoretisch hilft das Versions Schema von RPC dabei, eine Fehlkommunikation zwischen geänderten Servern und Clients und ihren bereitgestellten Gegenstücken zu verhindern. In der Praxis müssen Entwickler jedoch häufig Änderungen an vorhandenen Schnittstellen vornehmen, ohne die Version zu ändern, da vorherige Clients und Server in der Lage sein müssen, mit neuen zu kommunizieren. Dies ist ein größeres Problem für Standard-RPC als für com. Abfragen stellen eine natürliche Möglichkeit dar, in com nach unterstützten Schnittstellen zu suchen, während die RPC-Ausnahmebehandlung für eine äquivalente Abdeckung verwendet werden muss.

In diesem Abschnitt werden die besten RPC-Programmiermethoden zum Behandeln dieser Situationen erläutert. Dieser Abschnitt ist in die folgenden Themen unterteilt:

-   [Die versionierungstheorie für RPC und com](the-versioning-theory-for-rpc-and-com.md)
-   [Ändern von Schnittstellen in abwärts kompatibler Weise](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Beispiele für inkompatible Änderungen](examples-of-incompatible-changes.md)

 

 




