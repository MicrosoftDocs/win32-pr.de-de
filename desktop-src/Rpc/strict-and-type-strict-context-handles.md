---
title: Strict-und typstrikte Kontext Handles
description: Verwenden Sie \_ \_ für alle Kontext Handles das strikte Kontext Handle-Attribut.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473693"
---
# <a name="strict-and-type-strict-context-handles"></a>Strict-und typstrikte Kontext Handles

Verwenden Sie für alle Kontext Handles das [**strikte \_ Kontext \_ handle**](/windows/desktop/Midl/strict-context-handle) -Attribut. Standardmäßig ist ein Kontext Handle keiner Schnittstelle zugeordnet. Dies bedeutet, dass ein Kontext Handle auf einer Schnittstelle erstellt und dann an einen anderen übermittelt werden kann. Dies ist ein einfacher Angriff, und viele RPC-Server können dies nicht verhindern.

Wenn zwei Schnittstellen im selben Prozess nebeneinander vorhanden sind, kann ein Angreifer ein Kontext Handle auf einer Schnittstelle öffnen und an einen anderen übergeben, wodurch möglicherweise die unerwarteten Daten durchlaufen werden. Viele Entwickler sind der Meinung, dass Ihre Software die einzige Schnittstelle in einem Prozess ist, aber meistens ist dies nicht der Fall, da sowohl das System als auch viele Komponenten von Drittanbietern RPC intern verwenden und diese Schnittstellen Kontext Handles erstellen können. Wenn das [**strikte \_ Kontext \_ handle**](/windows/desktop/Midl/strict-context-handle) -Attribut verwendet wird, stellt die RPC-Laufzeit sicher, dass ein auf einer Schnittstelle erstelltes Kontext nur an Methoden dieser Schnittstelle als Argument weitergegeben werden kann.

In Situationen, in denen eine Anwendung für Windows Vista entwickelt wurde, ist die Verwendung des [**Typs \_ Strict- \_ Kontext \_ handle**](/windows/desktop/Midl/type-strict-context-handle) verfügbar und wird empfohlen. Kontext Handles sind nicht standardmäßig mit einem bestimmten Typ verknüpft. Wenn im gleichen Prozess mehrere Typen von Kontext Handles verwendet werden, ist es möglich, dass ein böswilliger Client ein Kontext Handle anstelle eines anderen übergibt, um unerwünschte Ergebnisse zu erzielen. Durch die Verwendung des **Typs \_ Strict- \_ Kontext \_ handle** können Anwendungen die Konsistenz des Kontext Handles erzwingen und jede nicht übereinstimmende Kontext Handle-Typverwendung verhindern.

 

 