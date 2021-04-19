---
description: Smartcard-Ressourcen-Manager
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Smartcard-Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373229"
---
# <a name="smart-card-resource-manager"></a>Smartcard-Ressourcen-Manager

Der [*Smartcard*](../secgloss/s-gly.md) - [*Ressourcen-Manager*](../secgloss/r-gly.md) verwaltet den Zugriff auf [*Reader*](../secgloss/r-gly.md) und *Smartcards*. Um diese Ressourcen zu verwalten, führt Sie die folgenden Funktionen aus.

-   Identifiziert und verfolgt Ressourcen.
-   Ordnet Leser und Ressourcen über mehrere Anwendungen zu.
-   Unterstützt [*Transaktions*](../secgloss/t-gly.md) primitive für den Zugriff auf Dienste, die auf einer bestimmten Karte verfügbar sind.
    > [!Note]  
    > Dies ist ein wichtiger Punkt, da es sich bei den aktuellen Karten um Single Thread Geräte handelt, die oft die Ausführung mehrerer Befehle erfordern, um eine einzelne Funktion abzuschließen. [*Transaktionen*](../secgloss/t-gly.md) ermöglichen die Ausführung mehrerer Befehle ohne Unterbrechung. Dadurch wird sichergestellt, dass die zwischen [*Zustands*](../secgloss/s-gly.md) Informationen nicht beschädigt sind.

     

Auf den Ressourcen-Manager kann direkt über die Resource Manager-API oder indirekt über einen beliebigen [*smartcarddienstanbieter*](../secgloss/s-gly.md)zugegriffen werden.

Die Resource Manager-API ist eine Reihe von Windows-Funktionen, die einen direkten Zugriff auf die Dienste des Ressourcen-Managers bereitstellen. Eine Übersicht über die von der API bereitgestellten Windows-Funktionen finden Sie unter [Smartcard-Ressourcen-Manager-API](smart-card-resource-manager-api.md). Im Vergleich dazu verwenden smartcarddienstanbieter com-Schnittstellen.

Viele der Windows-Funktionen in der Resource Manager-API verfügen über äquivalente in den Eigenschaften und Methoden der COM-Schnittstellen des Smartcard-Dienstanbieters. Obwohl die meisten Anwendungsentwickler die Arbeit mit com vereinfachen, müssen einige Anwendungen weiterhin die Windows-Funktionen verwenden, um bestimmte Aufgaben auszuführen. Beispielsweise müssen Anwendungen, die die Liste der Leser oder Lesergruppen in der [*Smartcard-Datenbank*](../secgloss/s-gly.md)bearbeiten müssen, und diejenigen, die eine direkte Steuerung eines Readers benötigen, die Resource Manager-API verwenden. Die Dienste, die diese Funktionen bereitstellen, sind nur in den Windows-Funktionen verfügbar, nicht im com, das von den Dienstanbietern bereitgestellt wird.

Informationen dazu, wie der [*Ressourcen-Manager*](../secgloss/r-gly.md) in Windows implementiert wird, finden Sie unter [Ressourcen-Manager-Implementierung](resource-manager-implementation.md).

 

 
