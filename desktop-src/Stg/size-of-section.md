---
title: Größe des Abschnitts
description: Der Abschnitts Größen Datentyp gibt die Größe des Abschnitts in Byte an.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207328"
---
# <a name="size-of-section"></a>Größe des Abschnitts

Der Abschnitts Größen Datentyp gibt die Größe des Abschnitts in Byte an. Da es sich bei der Abschnitts Größe um die ersten 4 Bytes handelt, können Abschnitte als Bytearray kopiert werden. Die Abschnitts Größe sollte immer ein Vielfaches von vier sein.

Beispielsweise würde ein leerer Abschnitt, d. h. eine mit NULL-Eigenschaften darin, eine Byte Anzahl von acht (die **DWORD** -Byte Anzahl und die **DWORD** -Anzahl von Eigenschaften) enthalten. Der-Abschnitt enthält die 8 Bytes: **08 00 00 00 00 00 00 00**.

 

 




