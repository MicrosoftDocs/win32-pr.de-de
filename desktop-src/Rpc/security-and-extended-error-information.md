---
title: Sicherheitsinformationen und erweiterte Fehlerinformationen
description: Erweiterte Fehlerinformationen bieten sehr nützliche Daten bei der Behandlung eines RPC-Problems, aber viele dieser Daten werden von sicherheitsbewussten Organisationen als vertraulich betrachtet.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f246e86dee31ea5e755c45211e3bd949657cdf95c37bf6ab4de3706be09fdec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925687"
---
# <a name="security-and-extended-error-information"></a>Sicherheitsinformationen und erweiterte Fehlerinformationen

Erweiterte Fehlerinformationen bieten sehr nützliche Daten bei der Behandlung eines RPC-Problems, aber viele dieser Daten werden von sicherheitsbewussten Organisationen als vertraulich betrachtet. Unter Berücksichtigung solcher Sicherheitsprobleme sind erweiterte Fehlerinformationen standardmäßig deaktiviert.

Erweiterte Fehlerinformationen werden weiterhin generiert, wenn erweiterte Fehlerinformationen deaktiviert sind, die Informationen jedoch nie über Prozess- oder Computergrenzen hinweg übertragen werden. Bei diesem Ansatz können Fehlerinformationen von Tools verwendet werden, die Zugriff auf den Prozessadressraum haben, z. B. Debugger. Wenn sie aktiviert ist, werden erweiterte Fehlerinformationen generiert und können über Prozess- und Computergrenzen hinweg gesendet werden. Derzeit werden erweiterte Fehlerinformationen für verbindungsorientierte Protokollsequenzen und lokale RPC (LRPC) verwendet. Sie ist teilweise für Datagramme implementiert.

 

 




