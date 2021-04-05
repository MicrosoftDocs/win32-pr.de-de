---
title: Sicherheit und erweiterte Fehlerinformationen
description: Erweiterte Fehlerinformationen bieten sehr nützliche Daten, wenn Sie ein RPC-Problem beheben. solche Daten werden jedoch von sicherheitsbewussten Organisationen als vertraulich eingestuft.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713553"
---
# <a name="security-and-extended-error-information"></a>Sicherheit und erweiterte Fehlerinformationen

Erweiterte Fehlerinformationen bieten sehr nützliche Daten, wenn Sie ein RPC-Problem beheben. solche Daten werden jedoch von sicherheitsbewussten Organisationen als vertraulich eingestuft. Wenn solche Sicherheitsprobleme berücksichtigt werden, sind erweiterte Fehlerinformationen standardmäßig deaktiviert.

Erweiterte Fehlerinformationen werden immer noch generiert, wenn erweiterte Fehlerinformationen deaktiviert sind, aber die Informationen niemals über Prozess-oder Computer Grenzen hinweg übertragen werden. Diese Vorgehensweise ermöglicht es, dass Fehlerinformationen von Tools verwendet werden, die Zugriff auf den Prozess Adressraum haben, z. b. Debugger. Wenn diese aktiviert ist, werden erweiterte Fehlerinformationen generiert und können über Prozess-und Computer Grenzen hinweg gesendet werden. Zurzeit werden erweiterte Fehlerinformationen für Verbindungs orientierte Protokoll Sequenzen und lokales RPC (LRPC) verwendet. Es ist teilweise für Datagramme implementiert.

 

 




