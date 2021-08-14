---
title: Out-of-Band-Signalisierung
description: Anwendungen, die allgemeine Daten mithilfe des Verzeichnisses gemeinsam nutzen, können Out-of-Band-Signalisierung verwenden, um Sowohl Versionsabweichungen als auch Teilupdates zu vermeiden.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06aab6482c9ad7af8e7c9b505b528b3559adb81f990b4d83681e44f418fadc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185417"
---
# <a name="out-of-band-signaling"></a>Out-of-Band-Signalisierung

Anwendungen, die allgemeine Daten mithilfe des Verzeichnisses gemeinsam nutzen, können Out-of-Band-Signalisierung verwenden, um Sowohl Versionsabweichungen als auch Teilupdates zu vermeiden. Einfach ausgedrückt: Die sich ablösenden Anwendungen verwenden einen Mechanismus, der von der Verzeichnisreplikation getrennt ist, um sich gegenseitig über Änderungen in den freigegebenen gemeinsamen Daten zu informieren. Out-of-Band-Signalisierung ist am effektivsten, wenn sie in Kombination mit einem Versionierungsmechanismus verwendet wird. Dadurch kann der Partner die Änderung erkennen, um Remotepartner über die Version der freigegebenen Daten zu informieren, auf die gewartet werden soll.

Wenn sie zum RPC-Beispiel zurückkehren, das im Abschnitt "Versionsschiefe" des [Replikationsverhaltens in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)angegeben ist, kann der RPC-Server verbundene Clients zurückrufen, um sie über die Verschiebung auf einen neuen Server zu informieren: "Ich verschiebe mich. Bitte stehen Sie bei, die Replikation bringt Ihnen die neue Adresse in Kürze", damit der Client den Übergangszeitraum verarbeiten kann.

Anwendungen, die dieselbe Richtlinie erzwingen müssen, um miteinander zu kommunizieren, können Out-of-Band-Signalisierung verwenden, um sicherzustellen, dass eine neue Richtlinie erst angewendet wird, wenn sie von allen beteiligten Parteien empfangen wurde. Wenn beispielsweise die IPsec-Richtlinie (Internet Protocol Security) zwischen zwei Computern geändert wird, kann ein Agent auf dem Quellcomputer einen Agent auf dem Zielcomputer kontaktieren, um die Anwendung der geänderten Richtlinie auszuhandeln, wobei die Anwendung des Quellcomputers verzögert wird, bis der Zielcomputer die neue Richtlinie ebenfalls empfangen hat.

 

 




