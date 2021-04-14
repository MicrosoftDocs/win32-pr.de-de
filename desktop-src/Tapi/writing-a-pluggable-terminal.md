---
description: Normalerweise implementiert ein Medien Dienstanbieter (MSP) die Terminal Erstellung.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Schreiben eines austauschbaren Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526810"
---
# <a name="writing-a-pluggable-terminal"></a>Schreiben eines austauschbaren Terminals

Normalerweise implementiert ein Medien Dienstanbieter (MSP) die Terminal Erstellung. Ab Windows 2000 SP1 umfasst TAPI 3 austauschbare Terminals, mit denen eine Anwendung die Terminal Erstellung implementieren kann. Weitere Informationen zur Verwendung dieser Terminals finden Sie in der Übersicht über die [Implementierung von austauschbaren Terminals](implementing-pluggable-terminals.md) .

Austauschbare Terminals sollten nicht regelmäßig verwendet werden, da die vollständigen Funktionen eines Terminals nur verfügbar sind, wenn ein MSP ihn vollständig kennt. Außerdem sollten Sie nicht versuchen, austauschbare Terminals zu implementieren, es sei denn, Sie sind bereits mit dem Schreiben von Medien Dienstanbietern vertraut. Die Techniken und potenziellen Probleme sind sehr ähnlich.

Die Bereitstellung eines speziellen Beispiels für ein austauschbares Terminal ist derzeit für die Situation eines Konferenz Servers vorhanden, der nicht-Windows 2000 SP1-oder nicht-Multicast-H. 323-Clients zu TAPI 3 mehr Parteien-SDP/IP-Multicast Konferenzen hinzufügen muss.

 

 



