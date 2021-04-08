---
title: Neues in SNMP
description: SNMP unterstützt die Verwendung von IPv6 ab Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729784"
---
# <a name="new-in-snmp"></a>Neues in SNMP

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

SNMP unterstützt die Verwendung von IPv6 ab Windows Vista. SNMP unterstützt IPv6 jedoch nur für Netzwerke mit Windows Server 2008 und Windows Vista. Dies liegt daran, dass SNMP den aktualisierten Protokollstapel erfordert, der in diesen Betriebssystemen für die IPv6-Unterstützung verfügbar ist.

Die IPv6-Kommunikation schlägt fehl, es sei denn, Ihr Netzwerk ist allein ein Windows Server 2008-Netzwerk, auch wenn ein IPv6-Protokollstapel separat auf den Computern installiert ist, auf denen frühere Versionen von Windows ausgeführt werden. SNMP-Agents, die unter Windows Server 2003, oder Windows XP oder Windows 2000 ausgeführt werden, Antworten beispielsweise nur auf Abfragen, die an Ihre IPv4-Adressen gerichtet sind.

 

 