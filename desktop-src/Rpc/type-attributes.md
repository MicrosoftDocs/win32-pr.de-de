---
title: Typattribute
description: Remote Prozedur Aufruf (RPC) und die Attribute des Mittelwert Typs, die auf Typdeklarationen angewendet werden können.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858268"
---
# <a name="type-attributes"></a>Typattribute

Typattribute sind die Mittelwert Attribute, die auf Typdeklarationen angewendet werden können:

-   **\[**[**bewältigen**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**Kontext \_ handle**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**\_Switchtyp**](/windows/desktop/Midl/switch-type)**\]**
-   [Zeiger-Typattribute](three-pointer-types.md)

Das **\[ \_ SwitchType \]** -Attribut gibt den Typ eines Union-Diskriminators an. Dieses Attribut gilt nur für eine nicht gekapselte Union.

Ein Kontext Handle ist ein Zeiger mit einem **\[ Kontext \_ handle \]** -Attribut. Das **\[ Kontext \_ handle \]** -Attribut ermöglicht es Ihnen, Prozeduren zu schreiben, die Zustandsinformationen zwischen Remote Prozedur aufrufen erhalten. Ein Kontext Handle mit einem Wert, der nicht NULL ist, stellt gespeicherten Kontext dar und dient zwei Zwecken:

-   Auf der Clientseite enthält Sie die Informationen, die von der RPC-Lauf Zeit Bibliothek benötigt werden, um den Aufruf an den Server weiterzuleiten.
-   Auf der Serverseite dient sie als Handle für den aktiven Kontext.

Das **\[** [**handle**](/windows/desktop/Midl/handle) - **\]** Attribut gibt an, dass ein Typ als benutzerdefiniertes (generisches) handle auftreten kann. Diese Funktion ermöglicht das Design von Handles, die für die Anwendung von Bedeutung sind. Der Benutzer muss Bindungs-und unbindungs Routinen bereitstellen, um zwischen dem benutzerdefinierten Handlertyp und dem primitiven RPC-Handle-Handle **\_ t** zu konvertieren. Ein Primitives Handle enthält Ziel Informationen, die für die RPC-Laufzeitbibliotheken von Bedeutung sind. Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einer Funktionsdeklaration. Ein Parameter mit dem **\[ handle \]** -Attribut hat einen doppelten Zweck. Sie wird verwendet, um die Bindung für den Aufruf zu bestimmen, und Sie wird als normaler Daten Parameter an die aufgerufene Prozedur übertragen.

 

 