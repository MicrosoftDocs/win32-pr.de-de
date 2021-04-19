---
description: Das Konzept der Blockierung in einer Windows-Umgebung war in der Vergangenheit ein sehr wichtiges Konzept.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Blockierende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372819"
---
# <a name="blocking-operations"></a>Blockierende Vorgänge

Das Konzept der Blockierung in einer Windows-Umgebung war in der Vergangenheit ein sehr wichtiges Konzept. In Windows Sockets 1,1-Umgebungen wurde das Blockieren von Aufrufen davon abgeraten, da Sie die laufende Interaktion mit dem System nicht mehr deaktivieren. Außerdem verwenden Sie eine Pseudo Blockierungs Methode, die aus verschiedenen Gründen nicht immer wie beabsichtigt funktioniert. In voremptiv geplanten Windows-Umgebungen sind blockierende Aufrufe jedoch viel sinnvoller, können durch systemeigene Betriebssystem Dienste implementiert werden und sind tatsächlich ein allgemein bevorzugter Mechanismus. Die Winsock 2-API unterstützt psuedoblockierungen nicht mehr, aber da die Windows Sockets 1,1-Kompatibilitäts-Shims weiterhin dieses Verhalten emulieren müssen, müssen die Dienstanbieter dies unterstützen, wie im folgenden beschrieben.

 

 



