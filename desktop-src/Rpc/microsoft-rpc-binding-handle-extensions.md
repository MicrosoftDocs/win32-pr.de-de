---
title: Microsoft RPC-Binding-Handle Erweiterungen
description: Die Microsoft-Erweiterungen der IDL-Sprache unterstützen mehrere handle-Parameter, die in anderen Positionen als dem ersten, äußersten linken Parameter angezeigt werden.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039753"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Microsoft RPC-Binding-Handle Erweiterungen

Die Microsoft-Erweiterungen der IDL-Sprache unterstützen mehrere handle-Parameter, die in anderen Positionen als dem ersten, äußersten linken Parameter angezeigt werden. In den folgenden Schritten wird die Sequenz beschrieben, die der-Mittelwert Compiler durchläuft, um den Bindungs handle-Parameter im DCE-Kompatibilitätsmodus (/**eines Zertifikats**) und im Standardmodus (Microsoft-erweiterter Modus) aufzulösen.

## <a name="dce-compatibility-mode"></a>DCE-Kompatibilitätsmodus

-   Bindungs handle, das an erster Stelle angezeigt wird.
-   Ganz links \[ [**in**](/windows/desktop/Midl/in), [**Kontext \_ handle**](/windows/desktop/Midl/context-handle) - \] Parameter.
-   Implizites Bindungs handle, das vom \[ [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ handle**](/windows/desktop/Midl/auto-handle)angegeben wird \] .
-   Wenn keine ACF vorhanden ist, wird die Verwendung des \[ **automatischen \_ Handles** standardmäßig verwendet \] .

## <a name="default-mode"></a>Standardmodus

-   Ganz links explizites Bindungs handle.
-   Implizites Bindungs handle, das vom \[ [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ handle**](/windows/desktop/Midl/auto-handle)angegeben wird \] .
-   Wenn keine ACF vorhanden ist, wird die Verwendung des \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)standardmäßig verwendet \] .

DCE-IDL-Compiler suchen nach einem expliziten Bindungs Handle als ersten Parameter. Wenn der erste Parameter kein Bindungs Handle und mindestens ein Kontext Handle angegeben ist, wird das äußerste Kontext Handle als Bindungs Handle verwendet. Wenn der erste Parameter kein Handle ist und keine Kontext Handles vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des \[ [**impliziten \_ Handles**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)des ACF-Attributs \] .

Die Microsoft-Erweiterungen für die IDL ermöglichen, dass das Bindungs Handle an einer anderen Position als der erste Parameter steht. Der am weitesten links stehende \[ [](/windows/desktop/Midl/in) \] Parameter des expliziten Handles – ob es sich um ein Primitives, vom Programmierer definiertes oder Kontext Handle handelt – ist das Bindungs handle. Wenn keine handle-Parameter vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des \[ [**impliziten \_ Handles**](/windows/desktop/Midl/implicit-handle) \] oder des \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)des ACF-Attributs \] .

Die folgenden Regeln gelten sowohl für den DCE-Kompatibilitätsmodus (/OSF) als auch für den Standardmodus:

-   Die automatische handle-Bindung wird verwendet, wenn keine ACF vorhanden ist.
-   Explizit \[ [**in**](/windows/desktop/Midl/in) \] oder \[ **in**, [**out**](/windows/desktop/Midl/out-idl) - \] Handles für eine einzelne Funktion vor allen impliziten Bindungen, die für die Schnittstelle angegeben sind.
-   Mehrere \[ [](/windows/desktop/Midl/in) \] primitive Handles in oder \[ **in** \] werden nicht unterstützt.
-   Mehrere \[ [](/windows/desktop/Midl/in) \] \[ explizite Kontext Handles in oder **in** \] sind zulässig.
-   Alle vom Programmierer definierten handle-Parameter Außer dem Parameter für den Bindungs handle werden als Daten behandelt, die für den Programmierer definiert sind.

Die folgende Tabelle enthält Beispiele, und es wird beschrieben, wie Bindungs Handles in den einzelnen compilermodi zugewiesen werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispiel</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td>Es wurde kein explizites handle angegeben. Das implizite Bindungs handle, das durch [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] oder [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>] angegeben wird, wird verwendet. Wenn keine ACF vorhanden ist, wird ein automatisches Handle verwendet.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td>Es wurde ein explizites Handle vom Typ handle_t angegeben. Der Parameter <em>H</em> ist das Bindungs Handle für die Prozedur.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td>Der erste Parameter ist kein handle. Im Standardmodus ist der am weitesten links stehende handle-Parameter <em>H</em>, der Bindungs handle. Im/OSF-Modus wird die implizite Bindung verwendet. Ein Fehler wird gemeldet, da der zweite Parameter als nicht zulässig erwartet wird und handle_t nicht übertragen werden können.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td>Der erste Parameter ist kein handle. Im Standardmodus ist der am weitesten links stehende handle-Parameter <em>H</em>, der Bindungs handle. Die stufs nennen die vom Benutzer bereitgestellten Routinen MY_HDL_bind und MY_HDL_unbind. Im/OSF-Modus wird die implizite Bindung verwendet. Der vom Programmierer definierte handle-Parameter <em>H</em> wird als nicht übertragbare Daten behandelt.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td>Der erste Parameter ist ein Bindungs handle. Der Parameter <em>H</em> ist der Bindungs handle-Parameter. Der zweite von einem Programmierer definierte handle-Parameter wird als Transaktionsdaten behandelt.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td>Das Bindungs Handle ist ein Kontext handle. Der Parameter <em>H</em> ist das Bindungs handle.</td>
</tr>
</tbody>
</table>



 

 

 