---
title: Microsoft RPC Binding-Handle Extensions
description: Die Microsoft-Erweiterungen für die IDL-Sprache unterstützen mehrere Handleparameter, die an anderen Positionen als dem ersten, am weitesten links angezeigten Parametern angezeigt werden.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c93b68b20628bf6f7f65cee026412846e0b497d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475366"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Microsoft RPC Binding-Handle Extensions

Die Microsoft-Erweiterungen für die IDL-Sprache unterstützen mehrere Handleparameter, die an anderen Positionen als dem ersten, am weitesten links angezeigten Parametern angezeigt werden. Die folgenden Schritte beschreiben die Sequenz, die der MIDL-Compiler durchläuft, um den Binding Handle-Parameter im DCE-Kompatibilitätsmodus (/**osf)** und im Standardmodus (Erweitert von Microsoft) aufzulösen.

## <a name="dce-compatibility-mode"></a>DCE-Kompatibilitätsmodus

-   Bindungshand handle, das an der ersten Position angezeigt wird.
-   Ganz links \[ [**in**](/windows/desktop/Midl/in), [**\_ Kontexthand handle-Parameter.**](/windows/desktop/Midl/context-handle) \]
-   Implizites Bindungshand handle, das \[ [**durch \_ implizites Handle oder**](/windows/desktop/Midl/implicit-handle) \] \[ [**automatisches Handle angegeben \_ wird.**](/windows/desktop/Midl/auto-handle) \]
-   Wenn kein ACF vorhanden ist, wird standardmäßig das automatische \[ **\_ Handle verwendet.** \]

## <a name="default-mode"></a>Standardmodus

-   Linkes, explizites Bindungshand handle.
-   Implizites Bindungshand handle, das \[ [**durch \_ implizites Handle oder**](/windows/desktop/Midl/implicit-handle) \] \[ [**automatisches Handle angegeben \_ wird.**](/windows/desktop/Midl/auto-handle) \]
-   Wenn kein ACF vorhanden ist, wird standardmäßig das automatische \[ [**\_ Handle verwendet.**](/windows/desktop/Midl/auto-handle) \]

DCE-IDL-Compiler suchen nach einem expliziten Bindungshandl als ersten Parameter. Wenn der erste Parameter kein Bindungshandles ist und mindestens ein Kontexthandles angegeben wird, wird das linke Kontexthandles als Bindungshandles verwendet. Wenn der erste Parameter kein Handle ist und es keine Kontexthandles gibt, verwendet die Prozedur die implizite Bindung mithilfe des impliziten Handles des ACF-Attributs \[ [**\_**](/windows/desktop/Midl/implicit-handle) oder \] des \[ [**automatischen \_ Handles.**](/windows/desktop/Midl/auto-handle) \]

Mit den Microsoft-Erweiterungen für die IDL kann sich das Bindungshandl an einer anderen Position als dem ersten Parameter positionieren. Der am \[ [**weitesten links im**](/windows/desktop/Midl/in) explicit-handle-Parameter – unabhängig davon, ob es sich um ein primitives, vom Programmierer definiertes oder Kontexthand handle handelt \] – ist das Bindungshand handle. Wenn keine Handleparameter enthalten sind, verwendet die Prozedur die implizite Bindung mithilfe des impliziten Handles des \[ [**\_ ACF-Attributs**](/windows/desktop/Midl/implicit-handle) \] oder des \[ [**automatischen \_ Handles.**](/windows/desktop/Midl/auto-handle) \]

Die folgenden Regeln gelten sowohl für den DCE-Kompatibilitätsmodus (/osf) als auch für den Standardmodus:

-   Die automatische Handlebindung wird verwendet, wenn kein ACF vorhanden ist.
-   Explizit \[ [**in**](/windows/desktop/Midl/in) oder in werden out-Handles für eine einzelne Funktion alle impliziten Bindungen, die \] für die Schnittstelle angegeben \[  [](/windows/desktop/Midl/out-idl) \] sind, vorab ausgeschlossen.
-   Mehrere \[ [**in oder**](/windows/desktop/Midl/in) \] \[ **in**, out primitive Handles \] werden nicht unterstützt.
-   Mehrere \[ [**in oder**](/windows/desktop/Midl/in) \] \[ **in** sind \] explizite Kontexthandles zulässig.
-   Alle vom Programmierer definierten Handleparameter mit Ausnahme des Binding Handle-Parameters werden als transmissible Daten behandelt.

Die folgende Tabelle enthält Beispiele und beschreibt, wie Bindungshandles in jedem Compilermodus zugewiesen werden.




| Beispiel | BESCHREIBUNG | 
|---------|-------------|
| <pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre> | Es wird kein explizites Handle angegeben. Das implizite Bindungshand handle, das durch [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] oder [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>] angegeben wird, wird verwendet. Wenn kein ACF vorhanden ist, wird ein automatisches Handle verwendet. | 
| <pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,           [in] short s );</code></pre> | Ein explizites Handle vom Typ handle_t angegeben. Der Parameter <em>H</em> ist das Bindungshand handle für die Prozedur. | 
| <pre class="syntax" data-space="preserve"><code>void proc3([in] short s,           [in] handle_t H );</code></pre> | Der erste Parameter ist kein Handle. Im Standardmodus ist der handle-Parameter am weitesten links, <em>H,</em>das Bindungshand handle. Im /osf-Modus wird die implizite Bindung verwendet. Ein Fehler wird gemeldet, da erwartet wird, dass der zweite Parameter transmissierbar ist und handle_t übertragen werden kann. | 
| <pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;void proc1([in] short s,           [in] MY_HDL H );</code></pre> | Der erste Parameter ist kein Handle. Im Standardmodus ist der handle-Parameter am weitesten links, <em>H,</em>das Bindungshand handle. Die Stubs rufen die vom Benutzer bereitgestellten Routinen MY_HDL_bind und MY_HDL_unbind. Im/Osf-Modus wird die implizite Bindung verwendet. Der vom Programmierer definierte Handleparameter <em>H</em> wird als transmissible Daten behandelt. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;void proc1([in] MY_HDL H,            [in] MY_HDL p );</code></pre> | Der erste Parameter ist ein Bindungshand handle. Der Parameter <em>H</em> ist der Binding-Handle-Parameter. Der zweite vom Programmierer definierte Handleparameter wird als transmissible Daten behandelt. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [context_handle] void * CTXT_HDL;void proc1([in] short s,           [in] long l,           [in] CTXT_HDL H ,           [in] char c);</code></pre> | Das Bindungshand handle ist ein Kontexthand handle. Der Parameter <em>H</em> ist das Bindungshand handle. | 




 

 

 
