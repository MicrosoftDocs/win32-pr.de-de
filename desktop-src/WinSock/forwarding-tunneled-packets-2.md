---
description: Der Code weist eine Einschränkung auf, die gekapselte (getunnerte) Pakete empfängt und Sie in eine bestimmte Schnittstelle demultipleert.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: IPv6-Weiterleitungs Tunneled-Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862568"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>IPv6-Weiterleitungs Tunneled-Pakete

Der Code weist eine Einschränkung auf, die gekapselte (getunnerte) Pakete empfängt und Sie in eine bestimmte Schnittstelle demultipleert. Wenn Sie über einen konfigurierten Tunnel empfangene getunnelt-Pakete weiterleiten möchten, müssen Sie die Weiterleitung an allen sechs über vier Schnittstellen und Schnittstelle \# 2 aktivieren. Das Aktivieren der Weiterleitung auf Schnittstelle \# 2 funktioniert nicht. Wenn Sie einen Router konfigurieren, aktivieren Sie in der Regel die Weiterleitung an allen Schnittstellen außer Loopback.

 

 



