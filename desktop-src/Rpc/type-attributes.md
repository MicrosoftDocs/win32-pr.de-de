---
title: Typattribute
description: Remote Procedure Call (RPC) und die MIDL-Typattribute, die auf Typdeklarationen angewendet werden können.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011168"
---
# <a name="type-attributes"></a>Typattribute

Typattribute sind die MIDL-Attribute, die auf Typdeklarationen angewendet werden können:

-   **\[**[**Behandeln**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**\_Kontexthandle**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**\_switch-Typ**](/windows/desktop/Midl/switch-type)**\]**
-   [Zeigertypattribute](three-pointer-types.md)

Das **\[ \_ \] Switchtypattribut** gibt den Typ eines Union-Diskriminators an. Dieses Attribut gilt nur für eine nicht gekapselte Union.

Ein Kontexthandle ist ein Zeiger mit einem **\[ \_ \] Kontexthandleat.** Mit dem **\[ \_ \] Kontexthandleattribut** können Sie Prozeduren schreiben, die Zustandsinformationen zwischen Remoteprozeduraufrufen verwalten. Ein Kontexthandle mit einem Wert ungleich NULL stellt gespeicherten Kontext dar und dient zwei Zwecken:

-   Auf clientseitiger Seite enthält sie die Informationen, die von der RPC-Laufzeitbibliothek benötigt werden, um den Aufruf an den Server weiterzuleiten.
-   Auf serverseitiger Seite dient es als Handle für aktiven Kontext.

Das **\[** [](/windows/desktop/Midl/handle) **\]** Handleattribut gibt an, dass ein Typ als benutzerdefiniertes (generisches) Handle auftreten kann. Dieses Feature ermöglicht das Entwerfen von Handles, die für die Anwendung von Bedeutung sind. Der Benutzer muss Bindungs- und Bindungsroutinen bereitstellen, um zwischen dem benutzerdefinierten Handletyp und dem primitiven RPC-Handletyp handle **\_ t** zu konvertieren. Ein primitives Handle enthält Zielinformationen, die für die RPC-Laufzeitbibliotheken von Bedeutung sind. Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einer Funktionsdeklaration. Ein Parameter mit dem **\[ \] Handleattribut** hat einen doppelten Zweck. Sie wird verwendet, um die Bindung für den Aufruf zu bestimmen, und sie wird als normaler Datenparameter an die aufgerufene Prozedur übertragen.

 

 