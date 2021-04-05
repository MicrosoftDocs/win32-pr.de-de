---
title: Sicherheitsmethoden
description: Microsoft RPC unterstützt zwei verschiedene Methoden zum Hinzufügen von Sicherheit zu ihrer verteilten Anwendung.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037415"
---
# <a name="security-methods"></a>Sicherheitsmethoden

Microsoft RPC unterstützt zwei verschiedene Methoden zum Hinzufügen von Sicherheit zu ihrer verteilten Anwendung. Die erste Methode ist die Verwendung der Security Support Provider-Schnittstelle (SSPI), auf die mithilfe der RPC-Funktionen zugegriffen werden kann. Im Allgemeinen empfiehlt es sich, diese Methode zu verwenden. Die SSPI bietet die flexibelsten und Netzwerk unabhängigen Authentifizierungs Features.

Die zweite Methode besteht darin, die Sicherheitsfunktionen zu verwenden, die in die System Transportprotokolle integriert sind. Die Sicherheitsmethode auf Transport Ebene ist nicht die bevorzugte Methode. Die Verwendung der SSPI wird empfohlen, da Sie für alle Transporte, plattformübergreifend, funktioniert und ein hohes Maß an Sicherheit bietet, einschließlich Datenschutz.

Dieser Abschnitt enthält Übersichten zu SSPI und Sicherheit auf Transport Ebene in den folgenden Themen:

-   [Security Support Provider Interface (SSPI)](security-support-provider-interface-sspi-.md)
-   [Transport Sicherheit](transport-security.md)

 

 




