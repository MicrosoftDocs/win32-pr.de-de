---
title: Strict- und Type Strict-Kontexthandles
description: Verwenden Sie das Strict \_ Context \_ Handle-Attribut für alle Kontexthandles.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c266fb70b540e08d066e51f61a921b8f88819456e83b909e3be31bb1f518c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017510"
---
# <a name="strict-and-type-strict-context-handles"></a>Strict- und Type Strict-Kontexthandles

Verwenden Sie das [**Strict \_ Context \_ Handle-Attribut**](/windows/desktop/Midl/strict-context-handle) für alle Kontexthandles. Standardmäßig ist ein Kontexthand handle nicht einer Schnittstelle zugeordnet, was bedeutet, dass ein Kontexthand handle auf einer Schnittstelle erstellt und dann an eine andere übergeben werden kann. Dies ist ein einfacher Angriff, und viele RPC-Server verhindern dies nicht.

Wenn zwei Schnittstellen im gleichen Prozess gleichzeitig bestehen, kann ein Angreifer ein Kontexthandler für eine Schnittstelle öffnen und an eine andere übergeben, die möglicherweise die unerwarteten Daten überflog. Viele Entwickler glauben, dass ihre Software die einzige Schnittstelle in einem Prozess ist, aber sehr oft ist dies nicht der Fall, da sowohl das System als auch viele Drittanbieterkomponenten RPC intern verwenden und diese Schnittstellen Kontexthandles erstellen können. Wenn das [**Strict \_ Context \_ Handle-Attribut**](/windows/desktop/Midl/strict-context-handle) verwendet wird, stellt die RPC-Laufzeit sicher, dass ein auf einer Schnittstelle erstellter Kontext nur als Argument an Methoden dieser Schnittstelle übergeben werden kann.

In Situationen, in denen eine Anwendung für Windows Vista entwickelt wird, ist die Verwendung eines typ [**\_ \_ \_ strict-Kontexthand**](/windows/desktop/Midl/type-strict-context-handle) handles verfügbar und wird empfohlen. Kontexthandles sind standardmäßig nicht einem bestimmten Typ zugeordnet. Wenn mehrere Typen von Kontexthandles im selben Prozess verwendet werden, kann ein böswilliger Client ein Kontexthandles statt eines anderen übergeben, um unerwünschte Ergebnisse zu erzeugen. Die Verwendung des **typ \_ \_ strict-Kontexthandpunkts \_** ermöglicht Es Anwendungen, die Typkonsistenz des Kontexthandpunkts zu erzwingen und eine nicht übereinstimmende Verwendung des Kontexthand handle-Typs zu verhindern.

 

 